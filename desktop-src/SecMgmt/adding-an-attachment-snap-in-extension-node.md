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
# <a name="adding-an-attachment-snap-in-extension-node"></a><span data-ttu-id="30d5e-103">Aggiunta di un nodo di estensione dello snap-in allegati</span><span class="sxs-lookup"><span data-stu-id="30d5e-103">Adding an Attachment Snap-in Extension Node</span></span>

<span data-ttu-id="30d5e-104">Quando il nodo viene espanso da un utente, un'estensione dello snap-in di un allegato deve essere aggiunta al nodo servizi.</span><span class="sxs-lookup"><span data-stu-id="30d5e-104">An attachment snap-in extension must add itself under the Services node when that node is expanded by a user.</span></span>

<span data-ttu-id="30d5e-105">Quando un utente espande il nodo servizi sotto uno degli snap-in di configurazione della sicurezza, MMC USA [**IComponentData:: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) e il \_ messaggio di notifica di MMCN Expand per inviare una notifica allo snap-in di configurazione della sicurezza, oltre a tutte le relative estensioni.</span><span class="sxs-lookup"><span data-stu-id="30d5e-105">When a user expands the Services node under one of the Security Configuration snap-ins, MMC uses [**IComponentData::Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) and the MMCN\_EXPAND notification message to notify the Security Configuration snap-in, plus all its extensions.</span></span>

<span data-ttu-id="30d5e-106">Lo snap-in di configurazione della sicurezza estrae quindi il formato interno da *lpDataObject*, che viene passato dal framework principale di MMC come tipo **lpDataObject**.</span><span class="sxs-lookup"><span data-stu-id="30d5e-106">The Security Configuration snap-in then extracts its internal format from the *lpDataObject*, which is passed in from the MMC main framework as type **LPDATAOBJECT**.</span></span> <span data-ttu-id="30d5e-107">Arresta l'elaborazione quando viene visualizzato il tipo di nodo servizi.</span><span class="sxs-lookup"><span data-stu-id="30d5e-107">It stops processing when it sees the Services node type.</span></span> <span data-ttu-id="30d5e-108">L'estensione dello snap-in allegati estrae quindi il tipo di nodo dal *lpDataObject*.</span><span class="sxs-lookup"><span data-stu-id="30d5e-108">The attachment snap-in extension then extracts the node type from the *lpDataObject*.</span></span> <span data-ttu-id="30d5e-109">Se il tipo di nodo è uno dei tipi di nodo definiti dal servizio, l'estensione dello snap-in allegati inserisce i nodi radice nel nodo padre specificato.</span><span class="sxs-lookup"><span data-stu-id="30d5e-109">If the node type is one of the service's defined node types, the attachment snap-in extension inserts its root nodes under the specified parent node.</span></span>

<span data-ttu-id="30d5e-110">Si noti che in questo esempio ExtractNodeType è una funzione privata implementata dall'estensione.</span><span class="sxs-lookup"><span data-stu-id="30d5e-110">Note that in this example, ExtractNodeType, is a private function that the extension implements.</span></span> <span data-ttu-id="30d5e-111">L'estensione esamina l'oggetto dati per ottenere il tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="30d5e-111">The extension examines the data object to get the node type.</span></span> <span data-ttu-id="30d5e-112">L'implementazione di ExtractNodeType non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="30d5e-112">The implementation of ExtractNodeType is not shown.</span></span>


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



 

 
