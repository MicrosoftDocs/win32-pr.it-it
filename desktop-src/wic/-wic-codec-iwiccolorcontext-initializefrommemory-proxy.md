---
description: Funzione proxy per il metodo InitializeFromMemory.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: Funzione IWICColorContext_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313429"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="194df-103">IWICColorContext \_ InitializeFromMemory- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="194df-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="194df-104">Funzione proxy per il metodo [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="194df-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="194df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="194df-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="194df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="194df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="194df-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="194df-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194df-108">Tipo: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _</span><span class="sxs-lookup"><span data-stu-id="194df-108">Type: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\** _</span></span>

</dd> <dt>

<span data-ttu-id="194df-109">_pbBuffer \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="194df-109">_pbBuffer\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194df-110">Tipo: \**const \* byte* _</span><span class="sxs-lookup"><span data-stu-id="194df-110">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="194df-111">Buffer utilizzato per inizializzare [_ *IWICColorContext* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="194df-111">The buffer used to initialize the [_ *IWICColorContext*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="194df-112">*cbBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="194df-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="194df-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="194df-113">Type: **UINT**</span></span>

<span data-ttu-id="194df-114">Dimensioni del buffer *pbBuffer* .</span><span class="sxs-lookup"><span data-stu-id="194df-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="194df-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="194df-115">Return value</span></span>

<span data-ttu-id="194df-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="194df-116">Type: **HRESULT**</span></span>

<span data-ttu-id="194df-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="194df-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="194df-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="194df-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="194df-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="194df-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="194df-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="194df-120">Requirements</span></span>



| <span data-ttu-id="194df-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="194df-121">Requirement</span></span> | <span data-ttu-id="194df-122">Valore</span><span class="sxs-lookup"><span data-stu-id="194df-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="194df-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="194df-123">Minimum supported client</span></span><br/> | <span data-ttu-id="194df-124">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="194df-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="194df-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="194df-125">Minimum supported server</span></span><br/> | <span data-ttu-id="194df-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="194df-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="194df-127">DLL</span><span class="sxs-lookup"><span data-stu-id="194df-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="194df-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="194df-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




