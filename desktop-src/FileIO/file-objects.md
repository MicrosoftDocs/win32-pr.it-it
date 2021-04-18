---
description: Gli oggetti file funzionano come interfaccia logica tra il kernel e i processi in modalità utente e i dati dei file che risiedono sul disco fisico.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Oggetti file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310025"
---
# <a name="file-objects"></a>Oggetti file

*Gli oggetti file* funzionano come interfaccia logica tra il kernel e i processi in modalità utente e i dati dei file che risiedono sul disco fisico. Un oggetto file contiene sia i dati scritti nel file che il seguente set di attributi gestiti dal kernel.



| Tipo di informazioni                                              | Scopo                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome file                                                     | Assegna un nome al file fisico corrispondente.                                                                                                                                                          |
| Offset di byte corrente                                           | Usato nell'I/O di file sincrono (descritto più avanti in questa sezione) per identificare il percorso di avvio corrente delle operazioni di lettura e scrittura.                                                          |
| Modalità condivisione                                                    | Specifica se un secondo processo può aprire un file per l'accesso in lettura, scrittura o eliminazione mentre il processo iniziale continua ad accedervi.                                                           |
| Modalità I/O                                                      | Specifica se il processo iniziale ha aperto il file per l'I/o [sincrono o asincrono](synchronous-and-asynchronous-i-o.md), l'i/o memorizzato nella cache o non memorizzato nella cache, l'i/o sequenziale o casuale e così via. |
| Puntatore all'oggetto dispositivo                                      | Identifica il dispositivo fisico in cui si trovano i dati del file.                                                                                                                                        |
| Puntatore al blocco di parametri del volume o [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifica il volume o la partizione in cui risiedono i dati del file.                                                                                                                                    |
| Puntatore a puntatori a oggetto sezione                            | Identifica una struttura radice che descrive un [file](/windows/desktop/Memory/file-mapping)di cui è stato eseguito il mapping.                                                                                                                  |
| Puntatore alla mappa della cache privata                                  | Identifica i dati del file attualmente memorizzati nella cache.                                                                                                                                              |



 

Questi attributi sono definiti come parte della struttura [**di \_ oggetti file**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) in ntddk. h. Fare riferimento alla definizione di questa struttura nella documentazione di Windows Driver Kit (WDK) per le lunghezze dei dati e i tipi di valori.

 

 
