---
description: Funzione proxy per il metodo SetMetadataByName.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: Funzione IWICMetadataQueryWriter_SetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316388"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="72922-103">IWICMetadataQueryWriter \_ SetMetadataByName- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="72922-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="72922-104">Funzione proxy per il metodo [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="72922-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72922-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72922-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="72922-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72922-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72922-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72922-108">Tipo: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="72922-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="72922-109">Puntatore a questo oggetto [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="72922-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="72922-110">*wzName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72922-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72922-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="72922-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="72922-112">Nome dell'elemento di metadati.</span><span class="sxs-lookup"><span data-stu-id="72922-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="72922-113">*pvarValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72922-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72922-114">Tipo: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="72922-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="72922-115">Metadati da impostare.</span><span class="sxs-lookup"><span data-stu-id="72922-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72922-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72922-116">Return value</span></span>

<span data-ttu-id="72922-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="72922-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="72922-118">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72922-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72922-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72922-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72922-120">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="72922-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="72922-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72922-121">Requirements</span></span>



| <span data-ttu-id="72922-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72922-122">Requirement</span></span> | <span data-ttu-id="72922-123">Valore</span><span class="sxs-lookup"><span data-stu-id="72922-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72922-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72922-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72922-125">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72922-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="72922-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72922-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72922-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72922-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="72922-128">DLL</span><span class="sxs-lookup"><span data-stu-id="72922-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72922-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72922-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

