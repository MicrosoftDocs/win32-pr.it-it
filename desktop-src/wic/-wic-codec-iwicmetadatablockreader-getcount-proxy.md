---
description: Funzione proxy per il metodo GetCount.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: Funzione IWICMetadataBlockReader_GetCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233023"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="5bc3e-103">\_Funzione proxy GetCount IWICMetadataBlockReader \_</span><span class="sxs-lookup"><span data-stu-id="5bc3e-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="5bc3e-104">Funzione proxy per il metodo [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) .</span><span class="sxs-lookup"><span data-stu-id="5bc3e-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc3e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bc3e-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="5bc3e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bc3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc3e-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bc3e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc3e-108">Tipo: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="5bc3e-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="5bc3e-109">Puntatore a questo oggetto [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="5bc3e-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="5bc3e-110">*pcCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bc3e-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc3e-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="5bc3e-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc3e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bc3e-112">Return value</span></span>

<span data-ttu-id="5bc3e-113">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5bc3e-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5bc3e-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5bc3e-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5bc3e-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5bc3e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc3e-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="5bc3e-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc3e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bc3e-117">Requirements</span></span>



| <span data-ttu-id="5bc3e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc3e-118">Requirement</span></span> | <span data-ttu-id="5bc3e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5bc3e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc3e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bc3e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc3e-121">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bc3e-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5bc3e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bc3e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc3e-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bc3e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5bc3e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5bc3e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc3e-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bc3e-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




