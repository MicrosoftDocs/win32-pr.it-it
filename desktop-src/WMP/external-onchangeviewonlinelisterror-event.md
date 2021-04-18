---
title: Evento External. OnChangeViewOnlineListError
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Media Player di Windows dell'evento External. OnChangeViewOnlineListError
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331228"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="b17fa-105">Evento External. OnChangeViewOnlineListError</span><span class="sxs-lookup"><span data-stu-id="b17fa-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="b17fa-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="b17fa-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b17fa-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b17fa-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b17fa-108">L'evento **OnChangeViewOnlineListError** si verifica quando una chiamata al metodo [External. changeViewOnlineList](external-changeviewonlinelist.md) genera un errore.</span><span class="sxs-lookup"><span data-stu-id="b17fa-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="b17fa-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b17fa-109">Possible Values</span></span>

<span data-ttu-id="b17fa-110">Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="b17fa-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="b17fa-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b17fa-111">Parameters</span></span>

<span data-ttu-id="b17fa-112">La funzione che gestisce questo errore presenta i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b17fa-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="b17fa-113"><span id="hr"></span><span id="HR"></span>*HR*</span><span class="sxs-lookup"><span data-stu-id="b17fa-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-114">Codice di errore **HRESULT** che indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="b17fa-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="b17fa-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="b17fa-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-116">La stessa stringa passata nel parametro **LibraryLocationType** di **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="b17fa-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="b17fa-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="b17fa-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-118">La stessa stringa passata nel parametro **LibraryLocationID** di **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="b17fa-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="b17fa-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="b17fa-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-120">La stessa stringa passata nel parametro **params** di **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="b17fa-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="b17fa-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="b17fa-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-122">La stessa stringa passata nel parametro **FriendlyName** di **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="b17fa-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="b17fa-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span><span class="sxs-lookup"><span data-stu-id="b17fa-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-124">La stessa stringa passata nel parametro **ListType** di **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="b17fa-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="b17fa-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="b17fa-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="b17fa-126">La stessa stringa passata nel parametro **ViewMode** di **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="b17fa-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b17fa-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b17fa-127">Requirements</span></span>



| <span data-ttu-id="b17fa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b17fa-128">Requirement</span></span> | <span data-ttu-id="b17fa-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b17fa-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b17fa-130">Versione</span><span class="sxs-lookup"><span data-stu-id="b17fa-130">Version</span></span><br/> | <span data-ttu-id="b17fa-131">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="b17fa-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="b17fa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b17fa-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="b17fa-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b17fa-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17fa-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b17fa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17fa-135">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="b17fa-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





