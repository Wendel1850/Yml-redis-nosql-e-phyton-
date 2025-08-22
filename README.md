import redis

redis_client = redis.Redis(host='localhost', port=6379, db=0)

# Inserir um valor
redis_client.set('nome', 'João')

# Buscar um valor
nome = redis_client.get('nome')
print(nome.decode('utf-8'))
