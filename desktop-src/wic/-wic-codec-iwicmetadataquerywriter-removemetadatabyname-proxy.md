---
description: Funzione proxy per il metodo RemoveMetadataByName.
ms.assetid: fb86766e-234d-4e39-9d4b-7814d50a3867
title: Funzione IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_RemoveMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e4681d3fbb93f176129ce2527356306d4ea02fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883174"
---
# <a name="iwicmetadataquerywriter_removemetadatabyname_proxy-function"></a><span data-ttu-id="cbb91-103">IWICMetadataQueryWriter \_ RemoveMetadataByName- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="cbb91-103">IWICMetadataQueryWriter\_RemoveMetadataByName\_Proxy function</span></span>

<span data-ttu-id="cbb91-104">Funzione proxy per il metodo [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="cbb91-104">Proxy function for the [**RemoveMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-removemetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbb91-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_RemoveMetadataByName_Proxy(
  _In_ IWICMetadataQueryWriter *THIS_PTR,
  _In_ LPCWSTR                 wzName
);
```



## <a name="parameters"></a><span data-ttu-id="cbb91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbb91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb91-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbb91-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb91-108">Tipo: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="cbb91-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="cbb91-109">Puntatore a questo oggetto [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="cbb91-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbb91-110">*wzName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbb91-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbb91-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="cbb91-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="cbb91-112">Nome dell'elemento di metadati da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cbb91-112">The name of the metadata item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbb91-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbb91-113">Return value</span></span>

<span data-ttu-id="cbb91-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cbb91-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cbb91-115">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cbb91-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cbb91-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbb91-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbb91-117">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="cbb91-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cbb91-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbb91-118">Requirements</span></span>



| <span data-ttu-id="cbb91-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb91-119">Requirement</span></span> | <span data-ttu-id="cbb91-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cbb91-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb91-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbb91-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb91-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbb91-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cbb91-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbb91-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb91-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbb91-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cbb91-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cbb91-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbb91-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbb91-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




