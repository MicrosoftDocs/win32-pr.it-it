---
description: Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt::P metodo rocessTransformCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878817"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a><span data-ttu-id="35e32-103">IItemPreviewerExt::P metodo rocessTransformCommand</span><span class="sxs-lookup"><span data-stu-id="35e32-103">IItemPreviewerExt::ProcessTransformCommand method</span></span>

<span data-ttu-id="35e32-104">Consente l'elaborazione di un comando di trasformazione rilevato in un modello di anteprima.</span><span class="sxs-lookup"><span data-stu-id="35e32-104">Permits processing of a transformation command encountered in a preview template.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35e32-105">Syntax</span></span>


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a><span data-ttu-id="35e32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35e32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e32-107">*dwContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e32-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e32-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="35e32-108">Type: **DWORD**</span></span>

<span data-ttu-id="35e32-109">Identificatore di contesto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="35e32-109">The context identifier for the operation.</span></span> <span data-ttu-id="35e32-110">Eseguire l'override dell'impostazione predefinita *dwContext* per impostare l'identificatore di contesto su un valore a scelta.</span><span class="sxs-lookup"><span data-stu-id="35e32-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="35e32-111">*pwszName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e32-111">*pwszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e32-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="35e32-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="35e32-113">Puntatore al nome del comando di trasformazione come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="35e32-113">A pointer to the name of the transformation command as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="35e32-114">*pwszArg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e32-114">*pwszArg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e32-115">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="35e32-115">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="35e32-116">Puntatore all'argomento come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="35e32-116">A pointer to the argument as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="35e32-117">*pvarResult* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="35e32-117">*pvarResult* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="35e32-118">Tipo: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="35e32-118">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="35e32-119">Puntatore alla variante di risultato.</span><span class="sxs-lookup"><span data-stu-id="35e32-119">A pointer to the result variant.</span></span> <span data-ttu-id="35e32-120">_pvarResult \* non deve essere un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="35e32-120">_pvarResult\* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e32-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35e32-121">Return value</span></span>

<span data-ttu-id="35e32-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="35e32-122">Type: **HRESULT**</span></span>

<span data-ttu-id="35e32-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="35e32-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35e32-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35e32-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e32-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="35e32-125">Remarks</span></span>

<span data-ttu-id="35e32-126">L'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="35e32-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="35e32-127">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="35e32-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e32-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35e32-128">Requirements</span></span>



| <span data-ttu-id="35e32-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e32-129">Requirement</span></span> | <span data-ttu-id="35e32-130">Valore</span><span class="sxs-lookup"><span data-stu-id="35e32-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35e32-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35e32-131">Minimum supported client</span></span><br/> | <span data-ttu-id="35e32-132">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35e32-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="35e32-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35e32-133">Minimum supported server</span></span><br/> | <span data-ttu-id="35e32-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35e32-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="35e32-135">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="35e32-135">Redistributable</span></span><br/>          | <span data-ttu-id="35e32-136">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="35e32-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="35e32-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35e32-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e32-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="35e32-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




