---
description: Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Metodo IWiaTransferCallback:: TransferCallback (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307351"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="62067-103">Metodo IWiaTransferCallback:: TransferCallback</span><span class="sxs-lookup"><span data-stu-id="62067-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="62067-104">Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento.</span><span class="sxs-lookup"><span data-stu-id="62067-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="62067-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62067-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="62067-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62067-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62067-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62067-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62067-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="62067-108">Type: **LONG**</span></span>

<span data-ttu-id="62067-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="62067-109">Currently unused.</span></span> <span data-ttu-id="62067-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="62067-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="62067-111">*pWiaTransferParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62067-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62067-112">Tipo: \**[**WiaTransferParams**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="62067-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="62067-113">Specifica un puntatore a una struttura [_ *WiaTransferParams* \*](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="62067-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62067-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62067-114">Return value</span></span>

<span data-ttu-id="62067-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="62067-115">Type: **HRESULT**</span></span>

<span data-ttu-id="62067-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62067-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62067-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62067-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62067-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="62067-118">Remarks</span></span>

<span data-ttu-id="62067-119">Quando questo metodo viene implementato da un filtro di elaborazione delle immagini, Windows Image Acquisition (WIA) 2,0 minidriver lo chiama durante l'acquisizione dell'immagine per inviare i messaggi di stato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62067-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="62067-120">Un filtro **IWiaTransferCallback:: TransferCallback** deve delegare al metodo **IWiaTransferCallback:: TransferCallback** del callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62067-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="62067-121">In genere, il flusso di filtro filtra i dati passati e scrive i dati filtrati direttamente nel flusso fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62067-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="62067-122">Quando il filtro di elaborazione delle immagini archivia i dati tra le chiamate al relativo metodo [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , deve anche modificare i valori *lPercentComplete* e *ulBytesWrittenToCurrentStream* nella struttura [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="62067-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="62067-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62067-123">Requirements</span></span>



| <span data-ttu-id="62067-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="62067-124">Requirement</span></span> | <span data-ttu-id="62067-125">Valore</span><span class="sxs-lookup"><span data-stu-id="62067-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62067-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62067-126">Minimum supported client</span></span><br/> | <span data-ttu-id="62067-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62067-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="62067-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62067-128">Minimum supported server</span></span><br/> | <span data-ttu-id="62067-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62067-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="62067-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62067-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="62067-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="62067-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="62067-132">IDL</span><span class="sxs-lookup"><span data-stu-id="62067-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62067-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62067-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="62067-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="62067-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="62067-135"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62067-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
