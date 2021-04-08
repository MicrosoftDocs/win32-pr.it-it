---
description: Funzione proxy per il metodo commit.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: Funzione IWICBitmapEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0cd3cfbe5e1c80d82cd90303d26f2da33cf467d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049455"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="c86fa-103">\_ \_ Funzione proxy commit IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="c86fa-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="c86fa-104">Funzione proxy per il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="c86fa-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c86fa-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="c86fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c86fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86fa-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c86fa-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86fa-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="c86fa-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="c86fa-109">Puntatore a questo oggetto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="c86fa-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86fa-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c86fa-110">Return value</span></span>

<span data-ttu-id="c86fa-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c86fa-111">Type: **HRESULT**</span></span>

<span data-ttu-id="c86fa-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c86fa-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c86fa-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c86fa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c86fa-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c86fa-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c86fa-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c86fa-115">Requirements</span></span>



| <span data-ttu-id="c86fa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c86fa-116">Requirement</span></span> | <span data-ttu-id="c86fa-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c86fa-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86fa-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c86fa-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c86fa-119">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c86fa-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c86fa-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c86fa-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c86fa-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c86fa-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c86fa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c86fa-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c86fa-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c86fa-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




