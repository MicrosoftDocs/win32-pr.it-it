---
description: Crea un oggetto di trasformazione colore che implementa IWICColorTransform. Questo oggetto COM supporta il modello a oggetti a thread libero.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: Funzione WICCreateColorTransform_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325697"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="397f5-104">\_Funzione proxy WICCreateColorTransform</span><span class="sxs-lookup"><span data-stu-id="397f5-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="397f5-105">Crea un oggetto di trasformazione colore che implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span><span class="sxs-lookup"><span data-stu-id="397f5-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="397f5-106">Questo oggetto COM supporta il modello a oggetti a thread libero.</span><span class="sxs-lookup"><span data-stu-id="397f5-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="397f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="397f5-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="397f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="397f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="397f5-109">*ppIColorTransform* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="397f5-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="397f5-110">Trasformazione colore creata.</span><span class="sxs-lookup"><span data-stu-id="397f5-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="397f5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="397f5-111">Return value</span></span>

<span data-ttu-id="397f5-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="397f5-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="397f5-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="397f5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="397f5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="397f5-114">Requirements</span></span>



| <span data-ttu-id="397f5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="397f5-115">Requirement</span></span> | <span data-ttu-id="397f5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="397f5-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="397f5-117">DLL</span><span class="sxs-lookup"><span data-stu-id="397f5-117">DLL</span></span><br/> | <dl> <span data-ttu-id="397f5-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="397f5-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 
