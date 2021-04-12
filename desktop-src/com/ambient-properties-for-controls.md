---
title: Proprietà di ambiente per i controlli
description: Proprietà di ambiente per i controlli
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396226"
---
# <a name="ambient-properties-for-controls"></a><span data-ttu-id="92e84-103">Proprietà di ambiente per i controlli</span><span class="sxs-lookup"><span data-stu-id="92e84-103">Ambient Properties for Controls</span></span>

<span data-ttu-id="92e84-104">Se un controllo supporta tutte le proprietà di ambiente, deve almeno rispettare i valori delle proprietà di ambiente seguenti in base alle condizioni indicate nella tabella seguente usando i DISPID standard.</span><span class="sxs-lookup"><span data-stu-id="92e84-104">If a control supports any ambient properties at all, it must at least respect the values of the following ambient properties under the conditions stated in the following table using the standard dispids.</span></span>



| <span data-ttu-id="92e84-105">Proprietà di ambiente</span><span class="sxs-lookup"><span data-stu-id="92e84-105">Ambient Property</span></span>            | <span data-ttu-id="92e84-106">DISPID</span><span class="sxs-lookup"><span data-stu-id="92e84-106">Dispid</span></span>          | <span data-ttu-id="92e84-107">Commento/condizioni per l'utilizzo</span><span class="sxs-lookup"><span data-stu-id="92e84-107">Comment/Conditions for Use</span></span>                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e84-108">LocaleID</span><span class="sxs-lookup"><span data-stu-id="92e84-108">LocaleID</span></span><br/>         | <span data-ttu-id="92e84-109">-705</span><span class="sxs-lookup"><span data-stu-id="92e84-109">-705</span></span><br/> | <span data-ttu-id="92e84-110">Se le impostazioni locali sono significative per il controllo, ad esempio per l'output di testo</span><span class="sxs-lookup"><span data-stu-id="92e84-110">If Locale is significant to the control, e.g. for text output</span></span><br/>                                                                                                                                                                                                                  |
| <span data-ttu-id="92e84-111">UserMode</span><span class="sxs-lookup"><span data-stu-id="92e84-111">UserMode</span></span> <br/>        | <span data-ttu-id="92e84-112">-709</span><span class="sxs-lookup"><span data-stu-id="92e84-112">-709</span></span><br/> | <span data-ttu-id="92e84-113">Se il controllo si comporta in modo diverso in modalità utente (progettazione) e modalità di esecuzione</span><span class="sxs-lookup"><span data-stu-id="92e84-113">If the control behaves differently in user (design) mode and run mode</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="92e84-114">UIDead</span><span class="sxs-lookup"><span data-stu-id="92e84-114">UIDead</span></span><br/>           | <span data-ttu-id="92e84-115">-710</span><span class="sxs-lookup"><span data-stu-id="92e84-115">-710</span></span><br/> | <span data-ttu-id="92e84-116">Se il controllo reagisce agli eventi dell'interfaccia utente, deve rispettare questa proprietà di ambiente</span><span class="sxs-lookup"><span data-stu-id="92e84-116">If the control reacts to UI events, then it should honor this ambient property</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="92e84-117">ShowGrabHandles</span><span class="sxs-lookup"><span data-stu-id="92e84-117">ShowGrabHandles</span></span><br/>  | <span data-ttu-id="92e84-118">-711</span><span class="sxs-lookup"><span data-stu-id="92e84-118">-711</span></span><br/> | <span data-ttu-id="92e84-119">Se il controllo supporta il ridimensionamento sul posto di se stesso</span><span class="sxs-lookup"><span data-stu-id="92e84-119">If the control support in-place resizing of itself</span></span><br/>                                                                                                                                                                                                                             |
| <span data-ttu-id="92e84-120">ShowHatching</span><span class="sxs-lookup"><span data-stu-id="92e84-120">ShowHatching</span></span><br/>     | <span data-ttu-id="92e84-121">-712</span><span class="sxs-lookup"><span data-stu-id="92e84-121">-712</span></span><br/> | <span data-ttu-id="92e84-122">Se il controllo supporta l'attivazione sul posto e l'attivazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="92e84-122">If the control support in-place activation and UI activation</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="92e84-123">DisplayAsDefault</span><span class="sxs-lookup"><span data-stu-id="92e84-123">DisplayAsDefault</span></span><br/> | <span data-ttu-id="92e84-124">-713</span><span class="sxs-lookup"><span data-stu-id="92e84-124">-713</span></span><br/> | <span data-ttu-id="92e84-125">Solo se il controllo è contrassegnato \_ come OLEMISC ACTSLIKEBUTTON (il che significa che viene fornito il supporto per i tasti di scelta rapida della tastiera, quindi è necessario implementare [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemonico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) ).</span><span class="sxs-lookup"><span data-stu-id="92e84-125">Only if the control is marked OLEMISC\_ACTSLIKEBUTTON (which means that support for keyboard mnemonics is provided, thus [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) must be implemented).</span></span><br/> |



 

<span data-ttu-id="92e84-126">Come descritto in precedenza, l'uso di ambienti richiede sia [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (per [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) come minimo) che [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (per [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) e [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span><span class="sxs-lookup"><span data-stu-id="92e84-126">As described previously, use of ambients requires both [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (for [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) as a minimum) as well as [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (for [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) and [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).</span></span>

<span data-ttu-id="92e84-127">Il \_ bit SETCLIENTSITEFIRST di OLEMISC potrebbe non essere necessariamente supportato da un contenitore.</span><span class="sxs-lookup"><span data-stu-id="92e84-127">The OLEMISC\_SETCLIENTSITEFIRST bit may not necessarily be supported by a container.</span></span> <span data-ttu-id="92e84-128">In questi casi, è necessario che un controllo ricorra ai valori predefiniti per le proprietà di ambiente necessarie.</span><span class="sxs-lookup"><span data-stu-id="92e84-128">In these circumstances, a control must resort to default values for the ambient properties that it requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92e84-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92e84-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e84-130">Controlli</span><span class="sxs-lookup"><span data-stu-id="92e84-130">Controls</span></span>](controls.md)
</dt> </dl>

 

 





