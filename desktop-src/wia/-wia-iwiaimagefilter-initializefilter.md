---
description: Inizializza il filtro. Chiamato da Windows Image Acquisition (WIA) 2,0 prima del download di ogni immagine.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Metodo IWiaImageFilter:: InitializeFilter (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312398"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="d6c18-104">Metodo IWiaImageFilter:: InitializeFilter</span><span class="sxs-lookup"><span data-stu-id="d6c18-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="d6c18-105">Inizializza il filtro.</span><span class="sxs-lookup"><span data-stu-id="d6c18-105">Initializes the filter.</span></span> <span data-ttu-id="d6c18-106">Chiamato da Windows Image Acquisition (WIA) 2,0 prima del download di ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="d6c18-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c18-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6c18-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="d6c18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6c18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c18-109">*pWiaItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c18-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c18-110">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d6c18-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="d6c18-111">Specifica un puntatore all'elemento [_ *IWiaItem2* \*](-wia-iwiaitem2.md) che rappresenta l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="d6c18-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="d6c18-112">*pWiaTransferCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6c18-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c18-113">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d6c18-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="d6c18-114">Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d6c18-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c18-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6c18-115">Return value</span></span>

<span data-ttu-id="d6c18-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6c18-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d6c18-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6c18-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6c18-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6c18-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c18-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6c18-119">Remarks</span></span>

<span data-ttu-id="d6c18-120">Questo metodo viene chiamato quando un'applicazione chiama [**download**](-wia-iwiatransfer-download.md) e quando un'applicazione chiama la funzione del componente WIA 2,0 Preview `GetNewPreview` .</span><span class="sxs-lookup"><span data-stu-id="d6c18-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="d6c18-121">**IWiaImageFilter:: InitializeFilter** archivia i riferimenti a *pWiaItem2* e *pWiaTransferCallback* per passare a queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="d6c18-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="d6c18-122">Questi due puntatori di interfaccia devono essere archiviati come variabili membro e [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve essere chiamato per ogni.</span><span class="sxs-lookup"><span data-stu-id="d6c18-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="d6c18-123">I puntatori di interfaccia sono necessari anche nell'implementazione del filtro di [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) e [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante l'acquisizione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d6c18-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c18-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6c18-124">Requirements</span></span>



| <span data-ttu-id="d6c18-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c18-125">Requirement</span></span> | <span data-ttu-id="d6c18-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d6c18-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c18-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c18-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c18-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6c18-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6c18-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6c18-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c18-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6c18-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d6c18-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6c18-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c18-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c18-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6c18-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d6c18-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6c18-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6c18-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
