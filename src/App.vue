<script setup>
    import { ref } from 'vue'
    const nome = ref('')
    const data = ref('')
    const email = ref('')
    const endereco = ref('')
    const cidade = ref('')
    const estado = ref('')
    const hobbie = ref('')
    const linguagem = ref('')
    const biografia = ref('')
    const senha = ref('')
    const confirma = ref('')
    const ok = ref(false)
    </script>
    
    
    <template>
      <div class="">
        <button>Nome:</button>
        <input type="text" v-model="nome" placeholder="Digite seu nome" />
        <p>O nome digitado é: {{ nome }}</p>
        
        <button>Data de nascimento:</button>
        <input type="text"  v-model="data" placeholder="Digite sua data" />
        <p>A data digitada é: {{ data }}</p>
        
        <button>Email:</button>
        <input type="email" v-model="email" placeholder="Digite seu email" 
        maxlength="5"/>
        <p>O email digitado é: {{ email }}</p>
        
        <button>Endereço:</button>
        <input type="text" v-model="endereco" placeholder="Digite seu endereço" />
        <p>O endereço digitado é: {{ endereco }}</p>
        
        <button>Cidade:</button>
        <input type="text"  v-model="cidade" placeholder="Digite sua cidade" />
        <p>A cidade digitada é: {{ cidade }}</p>
        
        <label for="estado" >Estado:</label>
        <select v-on:keypress="ok=false" v-model="estado">
          <option value="AC">Acre</option>
          <option value="AL">Alagoas</option>
          <option value="AP">Amapá</option>
          <option value="AM">Amazonas</option>
          <option value="BA">Bahia</option>
          <option value="CE">Ceará</option>
          <option value="DF">Distrito Federal</option>
          <option value="ES">Espírito Santo</option>
          <option value="GO">Goías</option>
          <option value="MA">Maranhão</option>
          <option value="MT">Mato Grosso</option>
          <option value="MS">Mato Grosso do Sul</option>
          <option value="MG">Minas Gerais</option>
          <option value="PA">Pará</option>
          <option value="PB">Paraíba</option>
          <option value="PE">Pernambuco</option>
          <option value="PI">Piauí</option>
          <option value="RJ">Rio de Janeiro</option>
          <option value="RN">Rio Grande do Norte</option>
          <option value="RS">Rio Grande do Sul</option>
          <option value="RO">Rondônia</option>
          <option value="RR">Roráima</option>
          <option value="SC">Santa Catarina</option>
          <option value="SP">São Paulo</option>
          <option value="SE">Sergipe</option>
          <option value="TO">Tocantins</option>
         </select>
        <p>O estado digitado é: {{ estado }}</p>
        
        <button>Hobbie:</button>
        <input type="text" v-on:keypress="ok=false" v-model="hobbie" placeholder="Digite seu hobbie" />
        <p>O hobbie digitado é: {{ hobbie }}</p>
        
        <button>Linguagem de programação:</button>
        <input type="text" v-on:keypress="ok=false" v-model="linguagem" placeholder="Digite sua linguagem" />
        <p>A linguagem digitada é: {{ linguagem }}</p>
        
        <button>Biografia:</button>
        <input type="text" v-on:keypress="ok=false" v-model="biografia" placeholder="Digite sua biografia" />
        <p>A biografia digitada é: {{ biografia }}</p>
        
        <button>Senha:</button>
        <input type="password" v-on:keypress="ok=false" v-model="senha" placeholder="Digite sua senha" />
        <p>A senha digitada é: {{ senha }}</p>
        
        <button>Confirmação de senha:</button>
        <input type="password" v-on:keypress="ok=false" v-model="confirma" placeholder="Digite sua senha novamente" />
        <p>A confirmação digitada é: {{ confirma }}</p>
        
        <button @click="ok = !ok">Mostrar</button>
      </div>
      <div v-if="ok">
        <p>O nome digitado é: {{ nome }}</p>
        <p>A data digitada é: {{ data }}</p>
        <p>O email digitado é: {{ email }}</p>
        <p>O endereço digitado é: {{ endereco }}</p>
        <p>A cidade digitada é: {{ cidade }}</p>
        <p>O estado digitado é: {{ estado }}</p>
        <p>O hobbie digitado é: {{ hobbie }}</p>
        <p>A linguagem digitada é: {{ linguagem }}</p>
        <p>A biografia digitada é: {{ biografia }}</p>
        <p>A senha digitada é: {{ senha }}</p>
        <p>A confirmação digitada é: {{ confirma }}</p> 
      </div>
    </template>

