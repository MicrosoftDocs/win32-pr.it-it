---
description: L'elenco seguente contiene i metodi CMSPStream chiamati dall'oggetto MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Metodi CMSPStream chiamati dall'oggetto MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b22461650be4e31298962a13194ed6ea1d69179023aa05b864d4d2585fe272b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868279"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>Metodi pubblici CMSPStream chiamati dall'oggetto MSPCall



| Metodi pubblici CMSPStream                                 | Descrizione                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Init**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Chiamato da **MSPCall** quando viene creato il flusso.                                   |
| [**Arresto**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Chiamato da **MSPCall per** deselezionare tutti gli oggetti terminale e rilasciare l'oggetto chiamata. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Chiamato dall'oggetto MSPCall per ottenere lo stato corrente del flusso.                   |
| [**HandleTSPData**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | L'oggetto chiamata derivato può chiamare questo metodo per consentire al flusso di gestire i comandi TSP.     |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Chiamato dall'oggetto MSPCall per consentire al flusso di gestire gli eventi del grafo.                     |



 

 

 



