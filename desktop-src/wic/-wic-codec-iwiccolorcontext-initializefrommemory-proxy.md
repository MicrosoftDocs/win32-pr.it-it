---
description: IWICColorContext_InitializeFromMemory_Proxy funzione proxy per il metodo InitializeFromMemory.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy funzione
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
ms.openlocfilehash: e77bbcf1e430891b031b2e77bc168c33f781eacf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097219"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="594e7-103">Funzione IWICColorContext \_ InitializeFromMemory \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="594e7-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="594e7-104">Funzione proxy per il [**metodo InitializeFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory)</span><span class="sxs-lookup"><span data-stu-id="594e7-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="594e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="594e7-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="594e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="594e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594e7-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="594e7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="594e7-108">Tipo: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="594e7-108">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

</dd> <dt>

<span data-ttu-id="594e7-109">*pbBuffer* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="594e7-109">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="594e7-110">Tipo: **const \* BYTE**</span><span class="sxs-lookup"><span data-stu-id="594e7-110">Type: **const BYTE\***</span></span>

<span data-ttu-id="594e7-111">Buffer utilizzato per inizializzare [**l'oggetto IWICColorContext.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)</span><span class="sxs-lookup"><span data-stu-id="594e7-111">The buffer used to initialize the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="594e7-112">*cbBufferSize* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="594e7-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="594e7-113">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="594e7-113">Type: **UINT**</span></span>

<span data-ttu-id="594e7-114">Dimensione del buffer *pbBuffer.*</span><span class="sxs-lookup"><span data-stu-id="594e7-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="594e7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="594e7-115">Return value</span></span>

<span data-ttu-id="594e7-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="594e7-116">Type: **HRESULT**</span></span>

<span data-ttu-id="594e7-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="594e7-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="594e7-118">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="594e7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="594e7-119">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="594e7-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="594e7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="594e7-120">Requirements</span></span>



| <span data-ttu-id="594e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="594e7-121">Requirement</span></span> | <span data-ttu-id="594e7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="594e7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="594e7-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="594e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="594e7-124">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="594e7-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="594e7-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="594e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="594e7-126">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="594e7-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="594e7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="594e7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="594e7-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="594e7-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




