---
title: Visualizzazione di finestre di dialogo
description: Visualizzazione di finestre di dialogo
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player Online Stores, visualizzazione di finestre di dialogo
- archivi online, visualizzazione di finestre di dialogo
- digitare 1 archivi online, visualizzare le finestre di dialogo
- Windows Media Player Online Stores, finestre di dialogo
- archivi online, finestre di dialogo
- digitare 1 archivi online, finestre di dialogo
- visualizzazione di finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723511"
---
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="18ba1-110">Visualizzazione di finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="18ba1-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="18ba1-111">L'archivio online può richiamare le finestre di dialogo tramite Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="18ba1-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="18ba1-112">A tale scopo, chiamare [External. ShowPopup](external-showpopup.md) dal codice dello script della pagina di individuazione, fornendo un valore di indice personalizzato che rappresenta la finestra di dialogo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="18ba1-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="18ba1-113">Il valore di indice è significativo solo per il codice del negozio online; Windows Media Player non interpreta questo valore.</span><span class="sxs-lookup"><span data-stu-id="18ba1-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="18ba1-114">Windows Media Player chiama quindi [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ PopupURL per il parametro *bstrInfoName* e il numero di indice per il parametro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="18ba1-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="18ba1-115">Il plug-in restituisce quindi un **BSTR** contenente l'URL della pagina Web da visualizzare nella finestra di dialogo e il lettore Visualizza la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="18ba1-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18ba1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18ba1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18ba1-117">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="18ba1-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




