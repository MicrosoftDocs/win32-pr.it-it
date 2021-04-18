---
title: Registrazione automatica per i controlli
description: Registrazione automatica per i controlli
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300528"
---
# <a name="self-registration-for-controls"></a><span data-ttu-id="60f12-103">Registrazione automatica per i controlli</span><span class="sxs-lookup"><span data-stu-id="60f12-103">Self Registration for Controls</span></span>

<span data-ttu-id="60f12-104">I controlli ActiveX devono supportare la registrazione automatica mediante l'implementazione delle funzioni [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) .</span><span class="sxs-lookup"><span data-stu-id="60f12-104">ActiveX controls must support self-registration by implementing the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="60f12-105">I controlli ActiveX devono registrare tutte le voci del registro di sistema standard per gli oggetti incorporabili e i server di automazione.</span><span class="sxs-lookup"><span data-stu-id="60f12-105">ActiveX controls must register all of the standard registry entries for embeddable objects and automation servers.</span></span>

<span data-ttu-id="60f12-106">I controlli ActiveX devono usare l'API delle categorie di componenti per registrarsi come controllo e registrare le categorie di componenti che richiedono un host per supportare e tutte le categorie implementate dal controllo, vedere [categorie di componenti](component-categories.md).</span><span class="sxs-lookup"><span data-stu-id="60f12-106">ActiveX controls must use the component categories API to register themselves as a control and register the component categories that they require a host to support and any categories that the control implements, see [Component Categories](component-categories.md).</span></span>

<span data-ttu-id="60f12-107">Anche i controlli ActiveX devono registrare la chiave del registro di sistema [ToolboxBitmap32](toolboxbitmap32.md) , anche se questa operazione non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="60f12-107">ActiveX controls should also register the [ToolBoxBitmap32](toolboxbitmap32.md) registry key, although this is not mandatory.</span></span>

<span data-ttu-id="60f12-108">La categoria di componenti inseribili deve essere registrata solo se il controllo è adatto per essere utilizzato come oggetto documento composto.</span><span class="sxs-lookup"><span data-stu-id="60f12-108">The Insertable component category should be registered only if the control is suitable for use as a compound document object.</span></span> <span data-ttu-id="60f12-109">È importante notare che un oggetto documento composto deve supportare determinate interfacce oltre il numero minimo di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) necessario per un controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="60f12-109">It is important to note that a compound document object must support certain interfaces beyond the minimum [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) required for an ActiveX control.</span></span> <span data-ttu-id="60f12-110">Sebbene un controllo ActiveX possa essere qualificato come oggetto documento composto, la documentazione del controllo deve indicare chiaramente il comportamento previsto in tali circostanze.</span><span class="sxs-lookup"><span data-stu-id="60f12-110">Although an ActiveX control may qualify as a compound document object, the control's documentation should clearly state what behavior to expect under these circumstances.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60f12-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60f12-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60f12-112">Controlli</span><span class="sxs-lookup"><span data-stu-id="60f12-112">Controls</span></span>](controls.md)
</dt> </dl>

 

 