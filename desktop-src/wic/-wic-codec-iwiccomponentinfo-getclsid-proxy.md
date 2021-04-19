---
description: Funzione proxy per il metodo getclsid.
ms.assetid: c6a8d752-590f-43d6-bac8-72b5bd259ad0
title: Funzione IWICComponentInfo_GetCLSID_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetCLSID_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc63d3f30605c0f5343502bcb96e989cc8496540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319560"
---
# <a name="iwiccomponentinfo_getclsid_proxy-function"></a><span data-ttu-id="93316-103">IWICComponentInfo \_ \_ funzione proxy getclsid</span><span class="sxs-lookup"><span data-stu-id="93316-103">IWICComponentInfo\_GetCLSID\_Proxy function</span></span>

<span data-ttu-id="93316-104">Funzione proxy per il metodo [**getclsid**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) .</span><span class="sxs-lookup"><span data-stu-id="93316-104">Proxy function for the [**GetCLSID**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getclsid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="93316-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93316-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetCLSID_Proxy(
  _In_  IWICComponentInfo *THIS_PTR,
  _Out_ CLSID             *pclsid
);
```



## <a name="parameters"></a><span data-ttu-id="93316-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93316-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93316-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93316-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="93316-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="93316-109">Puntatore a questo oggetto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="93316-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="93316-110">*pCLSID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93316-110">*pclsid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93316-111">Tipo: \**CLSID \** _</span><span class="sxs-lookup"><span data-stu-id="93316-111">Type: \**CLSID\** _</span></span>

<span data-ttu-id="93316-112">Puntatore che riceve il CLSID del componente.</span><span class="sxs-lookup"><span data-stu-id="93316-112">A pointer that receives the component's CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93316-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93316-113">Return value</span></span>

<span data-ttu-id="93316-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="93316-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="93316-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="93316-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93316-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93316-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93316-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="93316-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="93316-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93316-118">Requirements</span></span>



| <span data-ttu-id="93316-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93316-119">Requirement</span></span> | <span data-ttu-id="93316-120">Valore</span><span class="sxs-lookup"><span data-stu-id="93316-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93316-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93316-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93316-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93316-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="93316-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93316-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93316-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93316-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="93316-125">DLL</span><span class="sxs-lookup"><span data-stu-id="93316-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93316-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93316-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




