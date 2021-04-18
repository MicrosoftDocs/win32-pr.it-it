---
title: Evento External. OnChangeViewError
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Media Player di Windows dell'evento External. OnChangeViewError
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331229"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="2079e-105">Evento External. OnChangeViewError</span><span class="sxs-lookup"><span data-stu-id="2079e-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="2079e-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="2079e-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2079e-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2079e-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2079e-108">L'evento **OnChangeViewError** si verifica quando una chiamata al metodo [External. changeView](external-changeview.md) genera un errore.</span><span class="sxs-lookup"><span data-stu-id="2079e-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="2079e-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="2079e-109">Possible Values</span></span>

<span data-ttu-id="2079e-110">Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="2079e-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="2079e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2079e-111">Parameters</span></span>

<span data-ttu-id="2079e-112">La funzione che gestisce questo evento presenta i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2079e-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="2079e-113"><span id="hr"></span><span id="HR"></span>*HR*</span><span class="sxs-lookup"><span data-stu-id="2079e-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="2079e-114">Codice di errore **HRESULT** che indica il motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2079e-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="2079e-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="2079e-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="2079e-116">La stessa stringa passata nel parametro **LibraryLocationType** di **changeView**.</span><span class="sxs-lookup"><span data-stu-id="2079e-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="2079e-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="2079e-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="2079e-118">La stessa stringa questofosse passata nel parametro **LibraryLocationID** di **changeView**.</span><span class="sxs-lookup"><span data-stu-id="2079e-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="2079e-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtro*</span><span class="sxs-lookup"><span data-stu-id="2079e-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="2079e-120">La stessa stringa passata nel parametro **Filter** di **changeView**.</span><span class="sxs-lookup"><span data-stu-id="2079e-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="2079e-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span><span class="sxs-lookup"><span data-stu-id="2079e-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="2079e-122">La stessa stringa passata nel parametro **ViewParams** di **changeView**.</span><span class="sxs-lookup"><span data-stu-id="2079e-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2079e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2079e-123">Requirements</span></span>



| <span data-ttu-id="2079e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2079e-124">Requirement</span></span> | <span data-ttu-id="2079e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2079e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2079e-126">Versione</span><span class="sxs-lookup"><span data-stu-id="2079e-126">Version</span></span><br/> | <span data-ttu-id="2079e-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="2079e-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="2079e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2079e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="2079e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2079e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2079e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2079e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2079e-131">**ExternalObject per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="2079e-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





