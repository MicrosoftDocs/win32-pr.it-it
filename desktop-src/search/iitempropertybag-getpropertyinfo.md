---
description: Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Metodo IItemPropertyBag:: GetPropertyInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306102"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="98069-104">Metodo IItemPropertyBag:: GetPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="98069-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="98069-105">Ottiene le informazioni necessarie per leggere o salvare le proprietà nell'elenco delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="98069-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="98069-106">L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="98069-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="98069-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98069-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="98069-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="98069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98069-109">*IProperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98069-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98069-110">Indice in base zero della prima proprietà per la quale vengono richieste informazioni.</span><span class="sxs-lookup"><span data-stu-id="98069-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="98069-111">*cProperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98069-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98069-112">Numero di proprietà per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="98069-112">The number of properties to get information for.</span></span> <span data-ttu-id="98069-113">Questo argomento specifica il numero di elementi di matrice in *pPropBag*.</span><span class="sxs-lookup"><span data-stu-id="98069-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="98069-114">*pPropBag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98069-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98069-115">Puntatore a una matrice di strutture [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che riceve le informazioni per le proprietà.</span><span class="sxs-lookup"><span data-stu-id="98069-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="98069-116">*pcProperties* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="98069-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98069-117">Riceve un puntatore a una variabile **ULONG** che riceve il numero di proprietà per le quali sono state recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="98069-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98069-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98069-118">Return value</span></span>

<span data-ttu-id="98069-119">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="98069-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="98069-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98069-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98069-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="98069-121">Remarks</span></span>

<span data-ttu-id="98069-122">L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="98069-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="98069-123">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPropertyBag**](iitempropertybag.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem**](-search-isearchitem.md) , le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="98069-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="98069-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98069-124">Requirements</span></span>



| <span data-ttu-id="98069-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="98069-125">Requirement</span></span> | <span data-ttu-id="98069-126">Valore</span><span class="sxs-lookup"><span data-stu-id="98069-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98069-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98069-127">Minimum supported client</span></span><br/> | <span data-ttu-id="98069-128">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="98069-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98069-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98069-129">Minimum supported server</span></span><br/> | <span data-ttu-id="98069-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="98069-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="98069-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="98069-131">Redistributable</span></span><br/>          | <span data-ttu-id="98069-132">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="98069-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="98069-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98069-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98069-134">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="98069-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




