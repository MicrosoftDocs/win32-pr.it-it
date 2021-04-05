---
description: Quando il nodo viene espanso da un utente, un'estensione dello snap-in di un allegato deve essere aggiunta al nodo servizi.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Aggiunta di un nodo di estensione dello snap-in allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758036"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a>Aggiunta di un nodo di estensione dello snap-in allegati

Quando il nodo viene espanso da un utente, un'estensione dello snap-in di un allegato deve essere aggiunta al nodo servizi.

Quando un utente espande il nodo servizi sotto uno degli snap-in di configurazione della sicurezza, MMC USA [**IComponentData:: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) e il \_ messaggio di notifica di MMCN Expand per inviare una notifica allo snap-in di configurazione della sicurezza, oltre a tutte le relative estensioni.

Lo snap-in di configurazione della sicurezza estrae quindi il formato interno da *lpDataObject*, che viene passato dal framework principale di MMC come tipo **lpDataObject**. Arresta l'elaborazione quando viene visualizzato il tipo di nodo servizi. L'estensione dello snap-in allegati estrae quindi il tipo di nodo dal *lpDataObject*. Se il tipo di nodo è uno dei tipi di nodo definiti dal servizio, l'estensione dello snap-in allegati inserisce i nodi radice nel nodo padre specificato.

Si noti che in questo esempio ExtractNodeType è una funzione privata implementata dall'estensione. L'estensione esamina l'oggetto dati per ottenere il tipo di nodo. L'implementazione di ExtractNodeType non viene visualizzata.


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 
