---
description: Determina il salvataggio di una o più proprietà nel contenitore delle proprietà. L'interfaccia IItemPropertyBag è supportata solo in Windows XP e Windows Server 2003 e non deve più essere utilizzata.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Metodo IItemPropertyBag:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128507"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="60649-104">Metodo IItemPropertyBag:: Write</span><span class="sxs-lookup"><span data-stu-id="60649-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="60649-105">Determina il salvataggio di una o più proprietà nel contenitore delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="60649-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="60649-106">L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="60649-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="60649-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60649-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="60649-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="60649-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60649-109">*cProperties* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60649-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60649-110">Numero di proprietà da salvare.</span><span class="sxs-lookup"><span data-stu-id="60649-110">The number of properties to save.</span></span> <span data-ttu-id="60649-111">Questo argomento specifica il numero di elementi nelle matrici in *pPropBag* e *pvarValue*.</span><span class="sxs-lookup"><span data-stu-id="60649-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="60649-112">*pPropBag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60649-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60649-113">Puntatore a una matrice di strutture [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) che specifica le proprietà da salvare.</span><span class="sxs-lookup"><span data-stu-id="60649-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="60649-114">*pvarValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60649-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60649-115">Puntatore a una **variante** il cui tipo dipende dal tipo di dati delle informazioni sulla proprietà in esso contenute.</span><span class="sxs-lookup"><span data-stu-id="60649-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60649-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60649-116">Return value</span></span>

<span data-ttu-id="60649-117">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60649-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="60649-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60649-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="60649-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="60649-119">Remarks</span></span>

<span data-ttu-id="60649-120">L'interfaccia [**IItemPropertyBag**](iitempropertybag.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="60649-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="60649-121">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPropertyBag**](iitempropertybag.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) e [**ISearchItem**](-search-isearchitem.md) , le strutture [**LINKINFO**](-search-linkinfo.md) e [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="60649-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="60649-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60649-122">Requirements</span></span>



| <span data-ttu-id="60649-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60649-123">Requirement</span></span> | <span data-ttu-id="60649-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60649-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60649-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60649-125">Minimum supported client</span></span><br/> | <span data-ttu-id="60649-126">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="60649-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="60649-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60649-127">Minimum supported server</span></span><br/> | <span data-ttu-id="60649-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="60649-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="60649-129">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="60649-129">Redistributable</span></span><br/>          | <span data-ttu-id="60649-130">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="60649-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="60649-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60649-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60649-132">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="60649-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




