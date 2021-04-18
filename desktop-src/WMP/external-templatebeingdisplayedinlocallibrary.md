---
title: External. templateBeingDisplayedInLocalLibrary
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Media Player di Windows External. templateBeingDisplayedInLocalLibrary
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328407"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="13e19-105">External. templateBeingDisplayedInLocalLibrary</span><span class="sxs-lookup"><span data-stu-id="13e19-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="13e19-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="13e19-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="13e19-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="13e19-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="13e19-108">La proprietà **templateBeingDisplayedInLocalLibrary** indica se il feed rappresentato dalla pagina di individuazione corrente viene visualizzato nel controllo di visualizzazione ad albero della libreria locale.</span><span class="sxs-lookup"><span data-stu-id="13e19-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e19-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13e19-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="13e19-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="13e19-110">Possible Values</span></span>

<span data-ttu-id="13e19-111">Questa proprietà è un **valore booleano** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="13e19-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="13e19-112">**True** indica che il feed viene visualizzato nel controllo di visualizzazione ad albero della libreria locale.</span><span class="sxs-lookup"><span data-stu-id="13e19-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e19-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="13e19-113">Remarks</span></span>

<span data-ttu-id="13e19-114">Una pagina di individuazione che rappresenta un feed per una playlist dinamica può visualizzare un pulsante che consente all'utente di salvare il feed nella propria libreria locale.</span><span class="sxs-lookup"><span data-stu-id="13e19-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="13e19-115">Il salvataggio del feed, in questo contesto, significa che alcuni metadati vengono salvati nel computer dell'utente e il feed viene elencato sotto il nodo **playlist** nel controllo di visualizzazione albero libreria locale.</span><span class="sxs-lookup"><span data-stu-id="13e19-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="13e19-116">Lo script nella pagina di individuazione può controllare la proprietà **templateBeingDisplayedInLocalLibrary** per determinare se l'utente ha già salvato il feed nella libreria locale.</span><span class="sxs-lookup"><span data-stu-id="13e19-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="13e19-117">Se l'utente ha già salvato il feed, nella pagina di individuazione non verrà visualizzato il pulsante Salva.</span><span class="sxs-lookup"><span data-stu-id="13e19-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="13e19-118">Una pagina di individuazione che rappresenta un feed di radio deve controllare la proprietà **templateBeingDisplayedInLocalLibrary** per lo stesso motivo.</span><span class="sxs-lookup"><span data-stu-id="13e19-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e19-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13e19-119">Requirements</span></span>



| <span data-ttu-id="13e19-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e19-120">Requirement</span></span> | <span data-ttu-id="13e19-121">Valore</span><span class="sxs-lookup"><span data-stu-id="13e19-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13e19-122">Versione</span><span class="sxs-lookup"><span data-stu-id="13e19-122">Version</span></span><br/> | <span data-ttu-id="13e19-123">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="13e19-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="13e19-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13e19-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="13e19-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e19-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e19-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13e19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e19-127">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="13e19-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





