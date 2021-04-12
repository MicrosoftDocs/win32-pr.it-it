---
title: Enumerazione dei gruppi (RRAS)
description: Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione tra un protocollo di routing e il gestore del gruppo multicast.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3860c6876ed6ea5caef4941efcdd949eb9890d
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104472038"
---
# <a name="enumerating-groups"></a>Enumerazione dei gruppi

Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione tra un protocollo di routing e il gestore del gruppo multicast. Nella prima colonna sono descritte le azioni eseguite dal protocollo di routing e le risposte del protocollo di routing al gestore del gruppo multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast al protocollo di routing. La terza colonna presenta informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.



| Azione protocollo di routing                                                                                                                                                    | Azione gestione gruppi multicast                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ottenere un handle per un'enumerazione utilizzando la funzione [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) .                                                         | Restituisce un handle.                                                                                                                                                                                                                                                                                             |
| Ottenere uno o più gruppi utilizzando la funzione [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) .                                                             | Restituisce il numero di gruppi che si adattano al buffer fornito dal client. Se non è possibile restituire alcun gruppo nel buffer fornito, restituire \_ l'errore \_ buffer insufficiente e le dimensioni del buffer necessarie per restituire un gruppo.<br/> Restituisce un errore se non sono presenti altri \_ \_ \_ gruppi.<br/> |
| Se \_ \_ viene ricevuto un errore di buffer insufficiente, chiamare di nuovo la funzione [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) usando un buffer delle dimensioni indicate. |                                                                                                                                                                                                                                                                                                              |
| Continuare a chiamare la funzione [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) fino a quando \_ non \_ \_ viene ricevuto alcun altro elemento.                                   |                                                                                                                                                                                                                                                                                                              |
| Terminare il processo di enumerazione utilizzando la funzione [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) .                                                                   | Eliminare l'handle.                                                                                                                                                                                                                                                                                          |



 

 

 





