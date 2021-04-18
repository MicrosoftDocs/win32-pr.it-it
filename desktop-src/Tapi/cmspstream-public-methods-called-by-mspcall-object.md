---
description: Nell'elenco seguente sono inclusi i metodi CMSPStream chiamati dall'oggetto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Metodi CMSPStream chiamati dall'oggetto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314625"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>Metodi pubblici CMSPStream chiamati dall'oggetto MSPCall



| Metodi pubblici CMSPStream                                 | Descrizione                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Init**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Chiamato da **MSPCall** quando viene creato il flusso.                                   |
| [**Arresto**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Chiamato da **MSPCall** per deselezionare tutti gli oggetti Terminal e rilasciare l'oggetto call. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Chiamato dall'oggetto MSPCall per ottenere lo stato corrente del flusso.                   |
| [**HandleTSPData**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | L'oggetto chiamata derivato può chiamare questo metodo per consentire al flusso di gestire i comandi del TSP.     |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Chiamato dall'oggetto MSPCall per consentire al flusso di gestire gli eventi del grafo.                     |



 

 

 



