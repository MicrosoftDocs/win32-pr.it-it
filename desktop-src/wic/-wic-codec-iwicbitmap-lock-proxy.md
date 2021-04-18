---
description: Funzione proxy per il metodo Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: Funzione IWICBitmap_Lock_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306686"
---
# <a name="iwicbitmap_lock_proxy-function"></a><span data-ttu-id="bcfd1-103">Funzione del proxy di \_ blocco IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="bcfd1-103">IWICBitmap\_Lock\_Proxy function</span></span>

<span data-ttu-id="bcfd1-104">Funzione proxy per il metodo [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .</span><span class="sxs-lookup"><span data-stu-id="bcfd1-104">Proxy function for the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcfd1-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a><span data-ttu-id="bcfd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcfd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcfd1-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcfd1-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd1-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="bcfd1-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="bcfd1-109">Puntatore a questo oggetto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="bcfd1-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="bcfd1-110">*prcLock* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcfd1-110">*prcLock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd1-111">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="bcfd1-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="bcfd1-112">Rettangolo a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="bcfd1-112">The rectangle to be accessed.</span></span>

</dd> <dt>

<span data-ttu-id="bcfd1-113">_flags \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcfd1-113">_flags\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd1-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bcfd1-114">Type: **DWORD**</span></span>

<span data-ttu-id="bcfd1-115">Modalità di accesso che si desidera ottenere per il blocco.</span><span class="sxs-lookup"><span data-stu-id="bcfd1-115">The access mode you wish to obtain for the lock.</span></span>

</dd> <dt>

<span data-ttu-id="bcfd1-116">*ppILock* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bcfd1-116">*ppILock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd1-117">Tipo: **[ **IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span><span class="sxs-lookup"><span data-stu-id="bcfd1-117">Type: **[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***</span></span>

<span data-ttu-id="bcfd1-118">Puntatore che riceve la posizione di memoria bloccata.</span><span class="sxs-lookup"><span data-stu-id="bcfd1-118">A pointer that receives the locked memory location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcfd1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcfd1-119">Return value</span></span>

<span data-ttu-id="bcfd1-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bcfd1-120">Type: **HRESULT**</span></span>

<span data-ttu-id="bcfd1-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bcfd1-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bcfd1-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bcfd1-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcfd1-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="bcfd1-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfd1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcfd1-124">Requirements</span></span>



| <span data-ttu-id="bcfd1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcfd1-125">Requirement</span></span> | <span data-ttu-id="bcfd1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bcfd1-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcfd1-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcfd1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bcfd1-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcfd1-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bcfd1-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcfd1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bcfd1-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bcfd1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bcfd1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bcfd1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcfd1-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcfd1-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




