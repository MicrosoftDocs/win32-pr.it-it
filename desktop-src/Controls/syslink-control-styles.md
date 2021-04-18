---
title: Stili del controllo SysLink (CommCtrl. h)
description: Le costanti di stile seguenti vengono usate per la creazione di controlli SysLink.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327598"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="978a8-103">Stili del controllo SysLink</span><span class="sxs-lookup"><span data-stu-id="978a8-103">SysLink Control Styles</span></span>

<span data-ttu-id="978a8-104">Le costanti di stile seguenti vengono usate per la creazione di controlli SysLink.</span><span class="sxs-lookup"><span data-stu-id="978a8-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="978a8-105">Costante</span><span class="sxs-lookup"><span data-stu-id="978a8-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="978a8-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="978a8-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="978a8-107"><dt>**\_SecurityTransparent trasparente**</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="978a8-108">La modalità di combinazione dello sfondo è trasparente.</span><span class="sxs-lookup"><span data-stu-id="978a8-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="978a8-109"><dt>Garanzia di stato **\_ IGNORERETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="978a8-110">Quando il collegamento ha lo stato attivo della tastiera e l'utente preme INVIO, la sequenza di tasti viene ignorata dal controllo e passata alla finestra di dialogo host.</span><span class="sxs-lookup"><span data-stu-id="978a8-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="978a8-111"><dt>**con \_ prefisso di stato**</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="978a8-112">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="978a8-112">**Windows Vista**.</span></span> <span data-ttu-id="978a8-113">Se il testo contiene una e commerciale, viene considerato come un carattere letterale anziché come prefisso per un tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="978a8-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="978a8-114"><dt>Garanzia di stato **\_ USEVISUALSTYLE**</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="978a8-115">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="978a8-115">**Windows Vista**.</span></span> <span data-ttu-id="978a8-116">Il collegamento viene visualizzato nello stile di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="978a8-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="978a8-117"><dt>**USECUSTOMTEXT di garanzia \_**</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="978a8-118">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="978a8-118">**Windows Vista**.</span></span> <span data-ttu-id="978a8-119">Quando il controllo viene disegnato, viene inviata una notifica [ \_ CUSTOMTEXT Nm](nm-customtext.md) , in modo che l'applicazione possa fornire il testo in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="978a8-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="978a8-120"><dt>**diritto di garanzia a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="978a8-121">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="978a8-121">**Windows Vista**.</span></span> <span data-ttu-id="978a8-122">Il testo è giustificato a destra.</span><span class="sxs-lookup"><span data-stu-id="978a8-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="978a8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="978a8-123">Requirements</span></span>



| <span data-ttu-id="978a8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="978a8-124">Requirement</span></span> | <span data-ttu-id="978a8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="978a8-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="978a8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="978a8-126">Header</span></span><br/> | <dl> <span data-ttu-id="978a8-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="978a8-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





