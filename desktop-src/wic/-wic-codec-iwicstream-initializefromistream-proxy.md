---
description: Funzione proxy per il metodo InitializeFromIStream.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: Funzione IWICStream_InitializeFromIStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232890"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a><span data-ttu-id="8315c-103">IWICStream \_ InitializeFromIStream- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="8315c-103">IWICStream\_InitializeFromIStream\_Proxy function</span></span>

<span data-ttu-id="8315c-104">Funzione proxy per il metodo [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) .</span><span class="sxs-lookup"><span data-stu-id="8315c-104">Proxy function for the [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8315c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8315c-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a><span data-ttu-id="8315c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8315c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8315c-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8315c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8315c-108">Tipo: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="8315c-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="8315c-109">Puntatore a questo oggetto [_ *IWICStream* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="8315c-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="8315c-110">*pIStream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8315c-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8315c-111">Tipo: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="8315c-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="8315c-112">Flusso di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="8315c-112">The initialize stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8315c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8315c-113">Return value</span></span>

<span data-ttu-id="8315c-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8315c-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8315c-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8315c-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8315c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8315c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8315c-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8315c-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8315c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8315c-118">Requirements</span></span>



| <span data-ttu-id="8315c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8315c-119">Requirement</span></span> | <span data-ttu-id="8315c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8315c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8315c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8315c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8315c-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8315c-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8315c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8315c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8315c-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8315c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8315c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8315c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8315c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8315c-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

