# รันแบบง่ายที่สุด
รันไฟล์ *start.sh* เลย ถ้าให้รันแบบ background ใส่ -d ต่อท้ายตอนรัน
สคริปจะรัน 2 เว็บเลย port แก้ใน *docker-compose.yml* ได้เลย
# รันแยก
1. Build base image
   * ```docker build -t oph2017base -f ./BaseImage/Dockerfile ./BaseImage/```
2. Run Web image
   * ``` docker run -d --name oph2017web101 -v ./Web-101/src:/data/public -p 8888:80 oph2017base ```
   * ``` docker run -d --name oph2017web102 -v ./Web-102/src:/data/public -p 8889:80 oph2017base ```
