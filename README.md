# valida-o-de-cpf-e-cnpj
NOME DO CADASTRO DAS PESSOAS:

<script>
  function TestaCPF(strCPF) {
      var Soma;
      var Resto;
      Soma = 0;
    if (strCPF == "00000000000") return false;

    for (i=1; i<=9; i++) Soma = Soma + parseInt(strCPF.substring(i-1, i)) * (11 - i);
    Resto = (Soma * 10) % 11;

      if ((Resto == 10) || (Resto == 11))  Resto = 0;
      if (Resto != parseInt(strCPF.substring(9, 10)) ) return false;

    Soma = 0;
      for (i = 1; i <= 10; i++) Soma = Soma + parseInt(strCPF.substring(i-1, i)) * (12 - i);
      Resto = (Soma * 10) % 11;

      if ((Resto == 10) || (Resto == 11))  Resto = 0;
      if (Resto != parseInt(strCPF.substring(10, 11) ) ) return false;
      return true;
  }
  var strCPF = "12345678909";
  alert(TestaCPF(strCPF));
  </script>

<div class="col-md-2">
  <label class="control-label" for="inputSuccess1">tp. Pessoa</label>
  <select  data-toggle="tooltip" data-placement="bottom" title="selecione o tipo de pessoa" class="form-control input-sm"   id="cli_tppessoa"   name="cli_tppessoa" onchange="aplicaMascara(this.value)" >
  <option  value="TT">[ --selecione o tp de pessoa-- ]</option>                                    <option  value="1">Pessoa Física</option>
  <option  value="2">Pessoa Jurídica</option>
  </select>
  </div>

  <div class="col-md-2">
    <label class="control-label" for="inputSuccess1">tp.Consulta</label>
    <select  data-toggle="tooltip" data-placement="bottom" title="selecione o tipo de pessoa" class="form-control input-sm"   id="cli_tppessoa"   name="cli_tppessoa" onchange="aplicaMascara(this.value)" >
    <option  value="TT">[ --selecione o tp por CPF ou CNPJ -- ]</option>                                    <option  value="1">CPF</option>
    <option  value="2">CNPJ</option>
    </select>
    </div>

    <div class="col-md-2">
      <label class="control-label" for="inputSuccess1">tp.Nome e Local Residi</label>
      <select  data-toggle="tooltip" data-placement="bottom" title="selecione o tipo de pessoa" class="form-control input-sm"   id="cli_tppessoa"   name="cli_tppessoa" onchange="aplicaMascara(this.value)" >
      <option  value="TT">[ --selecione o tp do Nome e Local Residi-- ]</option>                                    <option  value="1">Pessoa Física</option>
      <option  value="2">Pessoa Jurídica</option>
      </select>
      </div>

      <div class="col-md-2">
        <label class="control-label" for="inputSuccess1">tp.CPF</label>
        <select  data-toggle="tooltip" data-placement="bottom" title="selecione o tipo de pessoa" class="form-control input-sm"   id="cli_tppessoa"   name="cli_tppessoa" onchange="aplicaMascara(this.value)" >
        <option  value="TT">[ --selecione o tp do CPF ]</option>                                    <option  value="1">Verdadeiro</option>
        <option  value="2">Falso</option>
        </select>
        </div>
