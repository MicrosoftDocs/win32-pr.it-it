---
title: Supporto per USB 3,0
description: Supporto per USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730759"
---
# <a name="support-for-usb-30"></a>Supporto per USB 3,0

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

In Windows 8 e Windows Server 2012 è stato aggiunto il supporto per USB 3,0. Questa operazione è stata eseguita aggiungendo un nuovo stack software per potenziare il controller host USB 3,0, denominato XHC (eXtensible Host Controller). Sono stati mantenuti la parità di interfaccia, il livello livello IRQL, il contesto del chiamante, lo stato di errore, la frequenza dei tentativi e così via. Non dovrebbe esserci alcuna differenza quando si interagisce con un dispositivo connesso tramite USB 2,0 rispetto a USB 3,0.

Tuttavia, se si sta scrivendo un driver per un nuovo dispositivo USB 3,0, è possibile optare per le nuove funzionalità USB 3,0.

## <a name="manifestation"></a>Manifestazione

I trasferimenti di dispositivi sono più veloci e la potenza viene consumata da un PC tramite dispositivi USB complessivi. Sussiste il rischio che i dispositivi USB esistenti non funzionino correttamente quando si è connessi a una porta USB 3,0. Questo problema non si verifica e non è previsto, ma poiché il software che alimenta USB 3,0 è nuovo, si tratta di un rischio.

 

 




