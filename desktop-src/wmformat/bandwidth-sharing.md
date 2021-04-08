---
title: Condivisione della larghezza di banda
description: Condivisione della larghezza di banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows Media Format SDK, condivisione della larghezza di banda
- ASF (Advanced Systems Format), condivisione della larghezza di banda
- ASF (formato avanzato dei sistemi), condivisione della larghezza di banda
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- condivisione della larghezza di banda, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046328"
---
# <a name="bandwidth-sharing"></a><span data-ttu-id="18654-110">Condivisione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="18654-110">Bandwidth Sharing</span></span>

<span data-ttu-id="18654-111">È possibile specificare i flussi in un file che, quando vengono riuniti, utilizzare una larghezza di banda inferiore rispetto alla somma delle frequenze di bit dichiarate combinate.</span><span class="sxs-lookup"><span data-stu-id="18654-111">You can specify streams in a file that, when taken together, use less bandwidth than the sum of their stated bit rates combined.</span></span> <span data-ttu-id="18654-112">Specificando la condivisione della larghezza di banda nel profilo, è necessario chiarire alla lettura delle applicazioni che la larghezza di banda disponibile necessaria per trasmettere il file non è quella che potrebbe sembrare.</span><span class="sxs-lookup"><span data-stu-id="18654-112">By specifying bandwidth sharing in the profile, you clarify to reading applications that the available bandwidth needed to stream the file is not what it might otherwise seem.</span></span>

<span data-ttu-id="18654-113">Nessuno degli oggetti di Windows Media Format SDK modifica il comportamento in risposta alle informazioni di condivisione della larghezza di banda, fornito esclusivamente in modo da consentire la lettura delle applicazioni quando si determina se un file può essere riprodotto con un recapito limitato della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="18654-113">None of the objects of the Windows Media Format SDK change their behavior in response to bandwidth sharing information, which is provided solely so that reading applications can take it into account when determining whether a file can be played with restricted bandwidth delivery.</span></span>

<span data-ttu-id="18654-114">La condivisione della larghezza di banda è configurata con un oggetto di condivisione della larghezza di banda e viene aggiunta a un profilo prima di iniziare a scrivere un file</span><span class="sxs-lookup"><span data-stu-id="18654-114">Bandwidth sharing is configured with a bandwidth sharing object and is added to a profile before beginning to write a file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18654-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18654-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18654-116">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="18654-116">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="18654-117">**Oggetto di condivisione della larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="18654-117">**Bandwidth Sharing Object**</span></span>](bandwidth-sharing-object.md)
</dt> <dt>

[<span data-ttu-id="18654-118">**Interfaccia IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="18654-118">**IWMBandwidthSharing Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="18654-119">**Interfaccia IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="18654-119">**IWMProfile3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[<span data-ttu-id="18654-120">**Uso della condivisione della larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="18654-120">**Using Bandwidth Sharing**</span></span>](using-bandwidth-sharing.md)
</dt> </dl>

 

 




