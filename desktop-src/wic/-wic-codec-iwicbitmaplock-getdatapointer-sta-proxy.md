---
description: Funzione proxy per il metodo GetDataPointer.
ms.assetid: 7256d6eb-cb7c-4067-8382-511d64da6825
title: Funzione IWICBitmapLock_GetDataPointer_STA_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetDataPointer_STA_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 957ae5974d65430bd39ea41f2e094e9f9c7efb06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319128"
---
# <a name="iwicbitmaplock_getdatapointer_sta_proxy-function"></a><span data-ttu-id="24a70-103">\_ \_ Funzione proxy sta IWICBitmapLock GetDataPointer \_</span><span class="sxs-lookup"><span data-stu-id="24a70-103">IWICBitmapLock\_GetDataPointer\_STA\_Proxy function</span></span>

<span data-ttu-id="24a70-104">Funzione proxy per il metodo [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) .</span><span class="sxs-lookup"><span data-stu-id="24a70-104">Proxy function for the [**GetDataPointer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getdatapointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a70-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24a70-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetDataPointer_STA_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbBufferSize,
  _Out_ BYTE           **ppbData
);
```



## <a name="parameters"></a><span data-ttu-id="24a70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24a70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a70-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24a70-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a70-108">Tipo: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="24a70-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="24a70-109">Puntatore a questo oggetto [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="24a70-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="24a70-110">*pcbBufferSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24a70-110">*pcbBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24a70-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="24a70-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="24a70-112">Puntatore che riceve le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="24a70-112">A pointer that receives the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="24a70-113">_ppbData \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24a70-113">_ppbData\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24a70-114">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="24a70-114">Type: **BYTE\*\***</span></span>

<span data-ttu-id="24a70-115">Puntatore che riceve un puntatore al pixel superiore sinistro nel rettangolo bloccato.</span><span class="sxs-lookup"><span data-stu-id="24a70-115">A pointer that receives a pointer to the top left pixel in the locked rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a70-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24a70-116">Return value</span></span>

<span data-ttu-id="24a70-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="24a70-117">Type: **HRESULT**</span></span>

<span data-ttu-id="24a70-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="24a70-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24a70-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24a70-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a70-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="24a70-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="24a70-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24a70-121">Requirements</span></span>



| <span data-ttu-id="24a70-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a70-122">Requirement</span></span> | <span data-ttu-id="24a70-123">Valore</span><span class="sxs-lookup"><span data-stu-id="24a70-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a70-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24a70-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24a70-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24a70-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="24a70-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24a70-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24a70-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24a70-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="24a70-128">DLL</span><span class="sxs-lookup"><span data-stu-id="24a70-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24a70-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24a70-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




