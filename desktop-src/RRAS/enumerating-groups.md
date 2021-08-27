---
title: Enumerazione dei gruppi (RRAS)
description: La tabella seguente riepiloga una serie di passaggi di un'interazione tra un protocollo di routing e il gestore di gruppi multicast.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df3731e8370a213636ea12ad2a9b072903908888eba6983909c01201c655ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101841"
---
# <a name="enumerating-groups"></a>Enumerazione dei gruppi

La tabella seguente riepiloga una serie di passaggi di un'interazione tra un protocollo di routing e il gestore di gruppi multicast. La prima colonna descrive le azioni eseguite dal protocollo di routing e le risposte del protocollo di routing al gestore di gruppi multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast al protocollo di routing. La terza colonna presenta eventuali informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.



| Azione del protocollo di routing                                                                                                                                                    | Azione di gestione del gruppo multicast                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ottenere un handle per un'enumerazione usando la [**funzione MgmGroupEnumerationStart.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)                                                         | Restituisce un handle.                                                                                                                                                                                                                                                                                             |
| Ottenere uno o più gruppi usando la [**funzione MgmGroupEnumerationGetNext.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)                                                             | Restituisce tutti i gruppi che rientrano nel buffer fornito dal client. Se non è possibile restituire alcun gruppo nel buffer fornito, restituire ERROR INSUFFICIENT BUFFER e le dimensioni del buffer necessarie \_ \_ per restituire un gruppo.<br/> Restituisce ERROR \_ NO MORE ITEMS quando non sono presenti altri \_ \_ gruppi.<br/> |
| Se viene ricevuto ERROR INSUFFICIENT BUFFER, chiamare di nuovo la \_ \_ funzione [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) usando un buffer delle dimensioni indicate. |                                                                                                                                                                                                                                                                                                              |
| Continuare a chiamare la [**funzione MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) finché non viene ricevuto ERROR \_ NO MORE \_ \_ ITEMS.                                   |                                                                                                                                                                                                                                                                                                              |
| Terminare il processo di enumerazione [**usando la funzione MgmGroupEnumerationEnd.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)                                                                   | Eliminare l'handle.                                                                                                                                                                                                                                                                                          |



 

 

 





