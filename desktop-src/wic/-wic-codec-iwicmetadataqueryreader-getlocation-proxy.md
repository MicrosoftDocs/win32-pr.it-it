---
description: Funzione proxy per il metodo getLocation.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: Funzione IWICMetadataQueryReader_GetLocation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319118"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a><span data-ttu-id="8190b-103">\_Funzione proxy getLocation IWICMetadataQueryReader \_</span><span class="sxs-lookup"><span data-stu-id="8190b-103">IWICMetadataQueryReader\_GetLocation\_Proxy function</span></span>

<span data-ttu-id="8190b-104">Funzione proxy per il metodo [**getLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .</span><span class="sxs-lookup"><span data-stu-id="8190b-104">Proxy function for the [**GetLocation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8190b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8190b-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a><span data-ttu-id="8190b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8190b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8190b-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8190b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8190b-108">Tipo: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="8190b-108">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="8190b-109">Puntatore a questo oggetto [_ *IWICMetadataQueryReader* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="8190b-109">Pointer to this [_ *IWICMetadataQueryReader*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="8190b-110">*cchMaxLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8190b-110">*cchMaxLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8190b-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8190b-111">Type: **UINT**</span></span>

<span data-ttu-id="8190b-112">Lunghezza del buffer *wzNamespace* .</span><span class="sxs-lookup"><span data-stu-id="8190b-112">The length of the *wzNamespace* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8190b-113">*wzNamespace* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8190b-113">*wzNamespace* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8190b-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8190b-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="8190b-115">Puntatore che riceve il percorso dello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="8190b-115">Pointer that receives the current namespace location.</span></span>

</dd> <dt>

<span data-ttu-id="8190b-116">_pcchActualLength \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8190b-116">_pcchActualLength\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8190b-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="8190b-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="8190b-118">Lunghezza effettiva del buffer necessaria per recuperare il percorso dello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="8190b-118">The actual buffer length needed to retrieve the current namespace location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8190b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8190b-119">Return value</span></span>

<span data-ttu-id="8190b-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8190b-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8190b-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8190b-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8190b-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8190b-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8190b-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8190b-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8190b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8190b-124">Requirements</span></span>



| <span data-ttu-id="8190b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8190b-125">Requirement</span></span> | <span data-ttu-id="8190b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8190b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8190b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8190b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8190b-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8190b-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8190b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8190b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8190b-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8190b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8190b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8190b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8190b-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8190b-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




