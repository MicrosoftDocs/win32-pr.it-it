---
description: Determina la lettura di una o più proprietà dall'elenco delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Metodo IItemPropertyBag:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342941"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="19003-104">Metodo IItemPropertyBag:: Read</span><span class="sxs-lookup"><span data-stu-id="19003-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="19003-105">Determina la lettura di una o più proprietà dall'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="19003-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="19003-106">L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="19003-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="19003-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19003-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="19003-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="19003-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19003-109">*cProperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19003-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19003-110">Numero di proprietà da leggere.</span><span class="sxs-lookup"><span data-stu-id="19003-110">The number of properties to read.</span></span> <span data-ttu-id="19003-111">Questo argomento specifica il numero di elementi nelle matrici in *pPropBag*, *pvarValue* e *phrError*.</span><span class="sxs-lookup"><span data-stu-id="19003-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="19003-112">*pPropBag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19003-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19003-113">Puntatore a una matrice di strutture [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che specifica le proprietà richieste.</span><span class="sxs-lookup"><span data-stu-id="19003-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="19003-114">*pvarValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19003-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19003-115">Riceve un puntatore che restituisce una matrice di strutture **Variant** che riceve i valori della proprietà.</span><span class="sxs-lookup"><span data-stu-id="19003-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="19003-116">*phrError* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="19003-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19003-117">Puntatore a una matrice di valori **HRESULT** che riceve il risultato di ogni lettura della proprietà.</span><span class="sxs-lookup"><span data-stu-id="19003-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="19003-118">In questa matrice devono essere presenti almeno gli elementi *cProperties* .</span><span class="sxs-lookup"><span data-stu-id="19003-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19003-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19003-119">Return value</span></span>

<span data-ttu-id="19003-120">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19003-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="19003-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19003-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19003-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="19003-122">Remarks</span></span>

<span data-ttu-id="19003-123">L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="19003-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="19003-124">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPropertyBag**](iitempropertybag.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem**](-search-isearchitem.md) , le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="19003-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="19003-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19003-125">Requirements</span></span>



| <span data-ttu-id="19003-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="19003-126">Requirement</span></span> | <span data-ttu-id="19003-127">Valore</span><span class="sxs-lookup"><span data-stu-id="19003-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19003-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19003-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19003-129">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="19003-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19003-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19003-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19003-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19003-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19003-132">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="19003-132">Redistributable</span></span><br/>          | <span data-ttu-id="19003-133">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="19003-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="19003-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19003-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19003-135">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="19003-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




