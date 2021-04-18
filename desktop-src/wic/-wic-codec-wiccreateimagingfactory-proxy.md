---
description: Funzione proxy per la creazione di IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: Funzione WICCreateImagingFactory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313419"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="b348f-103">\_Funzione proxy WICCreateImagingFactory</span><span class="sxs-lookup"><span data-stu-id="b348f-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="b348f-104">Funzione proxy per la creazione di [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="b348f-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="b348f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b348f-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="b348f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b348f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b348f-107">*SDKVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b348f-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b348f-108">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b348f-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="b348f-109">*ppIImagingFactory* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b348f-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b348f-110">Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="b348f-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b348f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b348f-111">Return value</span></span>

<span data-ttu-id="b348f-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b348f-112">Type: **HRESULT**</span></span>

<span data-ttu-id="b348f-113">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b348f-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b348f-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b348f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b348f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b348f-115">Remarks</span></span>

<span data-ttu-id="b348f-116">Questa funzione è un helper per la creazione di una factory WIC per il collegamento esplicito della DLL, necessaria per Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b348f-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="b348f-117">Nell'utilizzo normale è invece possibile utilizzare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (vedere le [class factory dell'API WIC](./-wic-api.md#class-factories)), dal momento che è sempre incluso in tutte le versioni più recenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="b348f-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="b348f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b348f-118">Requirements</span></span>



| <span data-ttu-id="b348f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b348f-119">Requirement</span></span> | <span data-ttu-id="b348f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b348f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b348f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b348f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b348f-122">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b348f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b348f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b348f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b348f-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b348f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b348f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b348f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b348f-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b348f-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

