---
description: IWICMetadataQueryReader_GetContainerFormat_Proxy funzione proxy per il metodo GetContainerFormat.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1fa2e34aa0e4cff05f6cdacc9cd1f340ff41af28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097139"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a><span data-ttu-id="a40d5-103">Funzione proxy IWICMetadataQueryReader \_ GetContainerFormat \_</span><span class="sxs-lookup"><span data-stu-id="a40d5-103">IWICMetadataQueryReader\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="a40d5-104">Funzione proxy per il [**metodo GetContainerFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat)</span><span class="sxs-lookup"><span data-stu-id="a40d5-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a40d5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a40d5-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a40d5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a40d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40d5-107">*QUESTO \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a40d5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a40d5-108">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span><span class="sxs-lookup"><span data-stu-id="a40d5-108">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***</span></span>

<span data-ttu-id="a40d5-109">Puntatore a [**questo oggetto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)</span><span class="sxs-lookup"><span data-stu-id="a40d5-109">Pointer to this [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="a40d5-110">*pguidContainerFormat* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a40d5-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a40d5-111">Tipo: **\* GUID**</span><span class="sxs-lookup"><span data-stu-id="a40d5-111">Type: **GUID\***</span></span>

<span data-ttu-id="a40d5-112">Puntatore che riceve il GUID del formato cointainer.</span><span class="sxs-lookup"><span data-stu-id="a40d5-112">Pointer that receives the cointainer format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a40d5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a40d5-113">Return value</span></span>

<span data-ttu-id="a40d5-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a40d5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="a40d5-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a40d5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a40d5-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a40d5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40d5-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a40d5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a40d5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a40d5-118">Requirements</span></span>



| <span data-ttu-id="a40d5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a40d5-119">Requirement</span></span> | <span data-ttu-id="a40d5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a40d5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a40d5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40d5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a40d5-122">Windows XP con SP2, solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a40d5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a40d5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40d5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a40d5-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a40d5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a40d5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a40d5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a40d5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a40d5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




