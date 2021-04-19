---
description: Funzione proxy per il metodo InitializeFromMemory.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: Funzione IWICStream_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319556"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="3c9e7-103">IWICStream \_ InitializeFromMemory- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="3c9e7-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="3c9e7-104">Funzione proxy per il metodo [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="3c9e7-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c9e7-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="3c9e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c9e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c9e7-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c9e7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9e7-108">Tipo: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="3c9e7-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="3c9e7-109">Puntatore a questo oggetto [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="3c9e7-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c9e7-110">*pbBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c9e7-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9e7-111">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="3c9e7-111">Type: \**BYTE\** _</span></span>

<span data-ttu-id="3c9e7-112">Puntatore al buffer utilizzato per inizializzare il flusso.</span><span class="sxs-lookup"><span data-stu-id="3c9e7-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="3c9e7-113">_cbBufferSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c9e7-113">_cbBufferSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c9e7-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3c9e7-114">Type: **DWORD**</span></span>

<span data-ttu-id="3c9e7-115">Dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="3c9e7-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c9e7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c9e7-116">Return value</span></span>

<span data-ttu-id="3c9e7-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3c9e7-117">Type: **HRESULT**</span></span>

<span data-ttu-id="3c9e7-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c9e7-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c9e7-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c9e7-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c9e7-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="3c9e7-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3c9e7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c9e7-121">Requirements</span></span>



| <span data-ttu-id="3c9e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c9e7-122">Requirement</span></span> | <span data-ttu-id="3c9e7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3c9e7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9e7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c9e7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c9e7-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c9e7-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3c9e7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c9e7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c9e7-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c9e7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3c9e7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3c9e7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c9e7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c9e7-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




