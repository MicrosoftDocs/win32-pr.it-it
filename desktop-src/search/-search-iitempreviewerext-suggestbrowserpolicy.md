---
description: Suggerisce che i criteri di sicurezza devono essere applicati al browser.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Metodo IItemPreviewerExt:: SuggestBrowserPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484428"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="e127f-103">Metodo IItemPreviewerExt:: SuggestBrowserPolicy</span><span class="sxs-lookup"><span data-stu-id="e127f-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="e127f-104">Suggerisce che i criteri di sicurezza devono essere applicati al browser.</span><span class="sxs-lookup"><span data-stu-id="e127f-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e127f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e127f-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e127f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e127f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e127f-107">*dwContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e127f-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e127f-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e127f-108">Type: **DWORD**</span></span>

<span data-ttu-id="e127f-109">Identificatore di contesto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e127f-109">The context identifier for the operation.</span></span> <span data-ttu-id="e127f-110">Eseguire l'override dell'impostazione predefinita *dwContext* per impostare l'identificatore di contesto su un valore a scelta.</span><span class="sxs-lookup"><span data-stu-id="e127f-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="e127f-111">*pdwFlags* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e127f-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e127f-112">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="e127f-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="e127f-113">Puntatore a un valore DWORD contenente i flag di verifica della verifica.</span><span class="sxs-lookup"><span data-stu-id="e127f-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="e127f-114">Il flag _ *BROWSERPOLICY \_ \_ contenuto non attendibile*\* Disabilita la possibilità che l'anteprima sia in grado di eseguire script o ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e127f-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="e127f-115">Il parametro *pdwFlags* non deve essere un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="e127f-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e127f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e127f-116">Return value</span></span>

<span data-ttu-id="e127f-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e127f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e127f-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e127f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e127f-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e127f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e127f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e127f-120">Remarks</span></span>

<span data-ttu-id="e127f-121">L'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) è supportata solo in Windows XP e windows Server 2003 e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e127f-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="e127f-122">Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti in computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**IItemPreviewerExt**](-search-iitempreviewerext.md) e le API seguenti: le interfacce [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem**](-search-isearchitem.md) , la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="e127f-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="e127f-123">L'utilizzo del flag di **\_ \_ contenuto non attendibile BROWSERPOLICY** è fortemente consigliato per disabilitare la possibilità che l'anteprima sia in grado di eseguire script o ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e127f-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="e127f-124">Il metodo **IItemPreviewerExt:: SuggestBrowserPolicy** può restituire informazioni sull'eventuale attendibilità dell'elemento visualizzato in anteprima.</span><span class="sxs-lookup"><span data-stu-id="e127f-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="e127f-125">In questo modo il controllo Trident del Visualizzatore anteprime eseguirà lo script e anche i controlli ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e127f-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="e127f-126">Poiché il Visualizzatore anteprime usa spesso file temporanei per generare l'anteprima, questa operazione può comportare l'esecuzione di script e codice imprevisti nell'area del computer locale.</span><span class="sxs-lookup"><span data-stu-id="e127f-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e127f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e127f-127">Requirements</span></span>



| <span data-ttu-id="e127f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e127f-128">Requirement</span></span> | <span data-ttu-id="e127f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e127f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e127f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e127f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e127f-131">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e127f-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e127f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e127f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e127f-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e127f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e127f-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e127f-134">Redistributable</span></span><br/>          | <span data-ttu-id="e127f-135">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="e127f-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e127f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e127f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e127f-137">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="e127f-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




