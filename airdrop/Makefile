IMAGE_NAME_AIRDROP_UI=airdropui
CONTAINER_NAME=my-app-container

.PHONY: build run stop clean
#cd folder name && works semicolon or next line was not working
airdrop-ui-build:
	cd frontend && docker build -t $(IMAGE_NAME_AIRDROP_UI) .

airdrop-ui-run:
	docker run -d --name $(IMAGE_NAME_AIRDROP_UI) -p 80:80 $(IMAGE_NAME_AIRDROP_UI)

airdrop-ui-stop:
	docker stop $(IMAGE_NAME_AIRDROP_UI) && docker rm $(IMAGE_NAME_AIRDROP_UI)

airdrop-ui-clean:
	docker rmi $(IMAGE_NAME_AIRDROP_UI)
