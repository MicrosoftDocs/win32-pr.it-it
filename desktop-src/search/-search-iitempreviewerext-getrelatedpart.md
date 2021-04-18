---
description: Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Metodo IItemPreviewerExt:: GetRelatedPart'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306166"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a><span data-ttu-id="1c49a-103">Metodo IItemPreviewerExt:: GetRelatedPart</span><span class="sxs-lookup"><span data-stu-id="1c49a-103">IItemPreviewerExt::GetRelatedPart method</span></span>

<span data-ttu-id="1c49a-104">Ottiene una parte del corpo correlata per l'incorporamento nel flusso MHTML di output.</span><span class="sxs-lookup"><span data-stu-id="1c49a-104">Gets a related body part for embedding into the output MHTML stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c49a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c49a-105">Syntax</span></span>


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1c49a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c49a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c49a-107">*dwContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c49a-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c49a-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1c49a-108">Type: **DWORD**</span></span>

<span data-ttu-id="1c49a-109">Identificatore di contesto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1c49a-109">The context identifier for the operation.</span></span> <span data-ttu-id="1c49a-110">Eseguire l'override dell'impostazione predefinita **dwContext** per impostare l'identificatore di contesto su un valore a scelta.</span><span class="sxs-lookup"><span data-stu-id="1c49a-110">Override the **dwContext** default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="1c49a-111">*pwszProp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c49a-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c49a-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="1c49a-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="1c49a-113">Puntatore alla proprietà del contenuto collegato come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c49a-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="1c49a-114">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c49a-114">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c49a-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1c49a-115">Type: **DWORD**</span></span>

<span data-ttu-id="1c49a-116">Valore long integer senza segno che contiene l'indice in base zero della parte corpo correlata.</span><span class="sxs-lookup"><span data-stu-id="1c49a-116">An unsigned long integer value that contains the zero-based index of the related body part.</span></span>

</dd> <dt>

<span data-ttu-id="1c49a-117">*pInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1c49a-117">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1c49a-118">Tipo: \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="1c49a-118">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="1c49a-119">Riceve un puntatore alla struttura [_ *LINKINFO* \*](-search-linkinfo.md) in cui il metodo restituisce informazioni sulla transazione.</span><span class="sxs-lookup"><span data-stu-id="1c49a-119">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="1c49a-120">*pInfo* non deve essere un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="1c49a-120">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c49a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c49a-121">Return value</span></span>

<span data-ttu-id="1c49a-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1c49a-122">Type: **HRESULT**</span></span>

<span data-ttu-id="1c49a-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1c49a-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c49a-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c49a-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c49a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c49a-125">Remarks</span></span>

<span data-ttu-id="1c49a-126">L'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="1c49a-126">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="1c49a-127">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="1c49a-127">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c49a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c49a-128">Requirements</span></span>



| <span data-ttu-id="1c49a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c49a-129">Requirement</span></span> | <span data-ttu-id="1c49a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1c49a-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c49a-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c49a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1c49a-132">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c49a-132">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c49a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c49a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1c49a-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c49a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1c49a-135">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1c49a-135">Redistributable</span></span><br/>          | <span data-ttu-id="1c49a-136">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="1c49a-136">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1c49a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c49a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c49a-138">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="1c49a-138">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




