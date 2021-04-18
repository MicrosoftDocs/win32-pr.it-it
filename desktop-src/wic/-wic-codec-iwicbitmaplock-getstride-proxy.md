---
description: Funzione proxy per il metodo getstride.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: Funzione IWICBitmapLock_GetStride_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316816"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="65e42-103">\_Funzione proxy Getstride IWICBitmapLock \_</span><span class="sxs-lookup"><span data-stu-id="65e42-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="65e42-104">Funzione proxy per il metodo [**getstride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) .</span><span class="sxs-lookup"><span data-stu-id="65e42-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e42-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65e42-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="65e42-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65e42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65e42-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65e42-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65e42-108">Tipo: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="65e42-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="65e42-109">Puntatore a questo oggetto [_ *IWICBitmapLock* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="65e42-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="65e42-110">*pcbStride* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="65e42-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65e42-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="65e42-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="65e42-112">Stride bitmap.</span><span class="sxs-lookup"><span data-stu-id="65e42-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65e42-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65e42-113">Return value</span></span>

<span data-ttu-id="65e42-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="65e42-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="65e42-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65e42-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65e42-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65e42-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65e42-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="65e42-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="65e42-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65e42-118">Requirements</span></span>



| <span data-ttu-id="65e42-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e42-119">Requirement</span></span> | <span data-ttu-id="65e42-120">Valore</span><span class="sxs-lookup"><span data-stu-id="65e42-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e42-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65e42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="65e42-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65e42-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="65e42-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65e42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="65e42-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65e42-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="65e42-125">DLL</span><span class="sxs-lookup"><span data-stu-id="65e42-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65e42-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65e42-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




