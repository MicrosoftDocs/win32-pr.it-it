---
title: Interfacce di archiviazione
description: Interfacce di archiviazione
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517151"
---
# <a name="storage-interfaces"></a><span data-ttu-id="b434f-103">Interfacce di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b434f-103">Storage Interfaces</span></span>

<span data-ttu-id="b434f-104">I contenitori di controlli devono essere in grado di supportare i controlli che implementano [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="b434f-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="b434f-105">Facoltativamente, un contenitore può supportare qualsiasi altra interfaccia di persistenza, ad esempio [**Metodo IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , per i controlli che forniscono supporto.</span><span class="sxs-lookup"><span data-stu-id="b434f-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="b434f-106">Una volta che un contenitore di controlli ActiveX ha scelto e inizializzato un'interfaccia di archiviazione da usare ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)e così via), l'interfaccia di archiviazione resterà l'interfaccia di archiviazione primaria per la durata del controllo, ovvero il controllo rimarrà in possesso dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b434f-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="b434f-107">Questa operazione non impedisce il salvataggio del contenitore in altre interfacce di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b434f-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="b434f-108">I contenitori di controlli ActiveX non devono supportare un meccanismo di salvataggio come testo, quindi l'uso di [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) e l'interfaccia lato contenitore associata [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="b434f-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) and the associated container-side interface [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b434f-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b434f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b434f-110">Contenitori</span><span class="sxs-lookup"><span data-stu-id="b434f-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 