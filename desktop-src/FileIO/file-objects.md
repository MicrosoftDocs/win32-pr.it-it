---
description: Gli oggetti file funzionano come interfaccia logica tra i processi kernel e in modalità utente e i dati dei file che risiedono sul disco fisico.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Oggetti file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263eae282f76195cc125848f13f43f5ee3d8f676cc6328b2d03db443e6f1deec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107471"
---
# <a name="file-objects"></a>Oggetti file

*Gli oggetti* file funzionano come interfaccia logica tra i processi kernel e in modalità utente e i dati dei file che risiedono sul disco fisico. Un oggetto file contiene sia i dati scritti nel file che il set seguente di attributi gestiti dal kernel.



| Tipo di informazioni                                              | Scopo                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome file                                                     | Nome del file fisico corrispondente.                                                                                                                                                          |
| Offset dei byte corrente                                           | Usato nell'I/O sincrono dei file (descritto più avanti in questa sezione) per identificare il percorso iniziale corrente delle operazioni di lettura e scrittura.                                                          |
| Modalità di condivisione                                                    | Specifica se un secondo processo può aprire un file per l'accesso in lettura, scrittura o eliminazione mentre il processo iniziale vi accede ancora.                                                           |
| Modalità di I/O                                                      | Specifica se il processo iniziale ha aperto il file per [operazioni di I/O](synchronous-and-asynchronous-i-o.md)sincrone o asincrone, I/O memorizzato nella cache o non memorizzato nella cache, I/O sequenziale o casuale e così via. |
| Puntatore all'oggetto dispositivo                                      | Identifica il dispositivo fisico in cui risiedono i dati del file.                                                                                                                                        |
| Puntatore al blocco di parametri del volume o [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifica il volume o la partizione in cui risiedono i dati del file.                                                                                                                                    |
| Puntatore ai puntatori agli oggetti sezione                            | Identifica una struttura radice che descrive un [file mappato.](/windows/desktop/Memory/file-mapping)                                                                                                                  |
| Puntatore alla mappa della cache privata                                  | Identifica i dati del file attualmente memorizzati nella cache.                                                                                                                                              |



 

Questi attributi sono definiti come parte della struttura [**FILE \_ OBJECT**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) in Ntddk.h. Fare riferimento alla definizione di questa struttura nella documentazione di Windows Driver Kit (WDK) per la lunghezza dei dati e i tipi dei valori.

 

 
