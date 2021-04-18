---
description: Le notifiche seguenti vengono inviate da SetupIterateCabinet. Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere notifiche.
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: Notifiche file CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3e4eb7645fc3603f026db6bde3ce92f2ed2ce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306512"
---
# <a name="cabinet-file-notifications"></a>Notifiche file CAB

Le notifiche seguenti vengono inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Per ulteriori informazioni sul formato e sull'utilizzo delle notifiche, vedere [notifiche](notifications.md).



| Notifica                                                        | Descrizione                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEextracted**](spfilenotify-fileextracted.md)   | Il file è stato estratto dal file CAB.                                  |
| [**\_FILEINCABINET SPFILENOTIFY**](spfilenotify-fileincabinet.md)   | Un file viene rilevato nell'archivio, l'applicazione vuole estrarla? |
| [**\_NEEDNEWCABINET SPFILENOTIFY**](spfilenotify-neednewcabinet.md) | Il file corrente viene continuato nel file CAB successivo.                             |



 

 

 



