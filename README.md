# Website de Estatísticas de estágios da UFSC (Universidade Federal de Santa Catarina)

Este projeto é uma iniciativa para criar um website que exibe estatísticas relacionadas aos estágios oferecidos pela Universidade Federal de Santa Catarina (UFSC). Os dados são coletados e organizados para fornecer informações úteis para estudantes.

### Características técnicas:

- **Frontend**: Desenvolvido utilizando Javascript e React. O frontend apenas formata e exibe os dados, sendo puramente estático. Hospedado com o plano gratuito do Vercel.
- **Backend**: Utiliza Python para a coleta de dados das fontes oficiais da UFSC (https://siare.sistemas.ufsc.br/publico/vagasEstagio.xhtml), utilizando a biblioteca BeautifulSoup para web scraping. Os dados são processados localmente (em minha própria máquina) com um cron job diário, e é feito o upsert diretamente no banco de dados da Supabase. O frontend consome os dados diretamente da Supabase, não há backend dinâmico.

