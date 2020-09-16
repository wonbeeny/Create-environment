# environment.yml (Conda 사용자의 경우) 및 requirements.txt (pip의 경우)

## Export requirements.txt
- conda(source) activate env_name 이후
$ pip freeze > requirements.txt

## requirements.txt 에서 동일한 가상 환경을 만들고 싶다면
1) using pip
$ pip install -r requirements.txt

2) using Conda
$ conda create --name <env_name> --file requirements.txt

## Export environment.yml
1) conda(source) activate env_name 이후
$ conda env export > environment.yml

2) 가상환경에 들어가지 않고
$ conda env export --name my_env_name > environment.yml

## environment.yml 에서 동일한 가상 환경을 만들고 싶다면
$ conda env create -f environment.yml


# 가상환경 비활성화
$ conda deactivate

# 가상환경 생성
$ conda --version

$ conda create --name YOUR_ENV_NAME python=python_version

# 가상환경 삭제
$ conda remove --name env_name --all