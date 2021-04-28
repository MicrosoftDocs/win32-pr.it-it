---
description: IWICStream_InitializeFromMemory_Proxy funzione proxy per il metodo InitializeFromMemory.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: IWICStream_InitializeFromMemory_Proxy funzione
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
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097129"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="d8463-103">Funzione proxy \_ IWICStream InitializeFromMemory \_</span><span class="sxs-lookup"><span data-stu-id="d8463-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="d8463-104">Funzione proxy per il [**metodo InitializeFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory)</span><span class="sxs-lookup"><span data-stu-id="d8463-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8463-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8463-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="d8463-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8463-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8463-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8463-108">Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span><span class="sxs-lookup"><span data-stu-id="d8463-108">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span></span>

<span data-ttu-id="d8463-109">Puntatore a [**questo oggetto IWICStream.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)</span><span class="sxs-lookup"><span data-stu-id="d8463-109">Pointer to this [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="d8463-110">*pbBuffer* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d8463-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8463-111">Tipo: **\* BYTE**</span><span class="sxs-lookup"><span data-stu-id="d8463-111">Type: **BYTE\***</span></span>

<span data-ttu-id="d8463-112">Puntatore al buffer utilizzato per inizializzare il flusso.</span><span class="sxs-lookup"><span data-stu-id="d8463-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="d8463-113">*cbBufferSize* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d8463-113">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8463-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8463-114">Type: **DWORD**</span></span>

<span data-ttu-id="d8463-115">Dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="d8463-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8463-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8463-116">Return value</span></span>

<span data-ttu-id="d8463-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8463-117">Type: **HRESULT**</span></span>

<span data-ttu-id="d8463-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d8463-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8463-119">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d8463-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8463-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d8463-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8463-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8463-121">Requirements</span></span>



| <span data-ttu-id="d8463-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8463-122">Requirement</span></span> | <span data-ttu-id="d8463-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d8463-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8463-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8463-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d8463-125">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d8463-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8463-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8463-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d8463-127">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8463-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8463-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d8463-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8463-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8463-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




