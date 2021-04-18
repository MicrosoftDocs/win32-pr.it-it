---
description: Consente all'estensione di contenuti avanzati per una proprietà.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Metodo IItemPreviewerExt:: GetLinkedContent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306167"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="41984-103">Metodo IItemPreviewerExt:: GetLinkedContent</span><span class="sxs-lookup"><span data-stu-id="41984-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="41984-104">Consente all'estensione di contenuti avanzati per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="41984-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="41984-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41984-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="41984-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41984-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41984-107">*dwContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41984-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41984-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="41984-108">Type: **DWORD**</span></span>

<span data-ttu-id="41984-109">Identificatore di contesto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="41984-109">The context identifier for the operation.</span></span> <span data-ttu-id="41984-110">Eseguire l'override dell'impostazione predefinita *dwContext* per impostare l'identificatore di contesto su un valore a scelta.</span><span class="sxs-lookup"><span data-stu-id="41984-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="41984-111">*pwszProp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41984-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41984-112">Tipo: **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="41984-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="41984-113">Puntatore alla proprietà del contenuto collegato come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="41984-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="41984-114">*pInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="41984-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="41984-115">Tipo: \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="41984-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="41984-116">Riceve un puntatore alla struttura [_ *LINKINFO* \*](-search-linkinfo.md) in cui il metodo restituisce informazioni sulla transazione.</span><span class="sxs-lookup"><span data-stu-id="41984-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="41984-117">*pInfo* non deve essere un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="41984-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41984-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41984-118">Return value</span></span>

<span data-ttu-id="41984-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="41984-119">Type: **HRESULT**</span></span>

<span data-ttu-id="41984-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41984-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41984-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41984-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41984-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="41984-122">Remarks</span></span>

<span data-ttu-id="41984-123">L'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="41984-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="41984-124">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="41984-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="41984-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41984-125">Requirements</span></span>



| <span data-ttu-id="41984-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="41984-126">Requirement</span></span> | <span data-ttu-id="41984-127">Valore</span><span class="sxs-lookup"><span data-stu-id="41984-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="41984-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41984-128">Minimum supported client</span></span><br/> | <span data-ttu-id="41984-129">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="41984-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="41984-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41984-130">Minimum supported server</span></span><br/> | <span data-ttu-id="41984-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41984-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="41984-132">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="41984-132">Redistributable</span></span><br/>          | <span data-ttu-id="41984-133">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="41984-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="41984-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41984-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41984-135">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="41984-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




