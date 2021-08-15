---
title: Pacchetti di risposta BITS
description: Pacchetti di risposta BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0a77cab49b990cc736b652382555861ecc569e030bb3ddd2bf255f717d455f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323561"
---
# <a name="bits-response-packets"></a>Pacchetti di risposta BITS

Nella tabella seguente sono elencati i pacchetti di risposta inviati al client BITS per i processi di caricamento e caricamento-risposta. La tabella elenca i pacchetti nella sequenza tipica che vengono inviati al client.



| Pacchetto di risposta                                      | Scopo                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ack for Ping](ack-for-ping.md)                     | Conferma la [richiesta Ping.](ping.md)                                                                                                                                                  |
| [Ack for Create-Session](ack-for-create-session.md) | Conferma la richiesta [Create-Session](create-session.md) e restituisce un identificatore di sessione che il client BITS usa in tutte le richieste successive per identificare questa sessione di trasferimento file. |
| [Ack for Fragment](ack-for-fragment.md)             | Conferma la richiesta [Fragment](fragment.md) e scrive il frammento nel file di caricamento nel server.                                                                                 |
| [Ack for Close-Session](ack-for-close-session.md)   | Conferma la [richiesta close-session](close-session.md) e rilascia tutte le risorse associate alla sessione.                                                                         |
| [Ack for Cancel-Session](ack-for-cancel-session.md) | Conferma la [richiesta Cancel-Session](cancel-session.md) e rilascia tutte le risorse associate alla sessione.                                                                       |



 

 

 




