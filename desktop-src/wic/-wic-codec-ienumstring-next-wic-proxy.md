---
description: 'Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Next.'
ms.assetid: a3f6a32b-3043-4bea-a70b-0b4507b4e3a1
title: Funzione IEnumString_Next_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Next_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ae3e25b355268fe63025692bf116b60b45122e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049457"
---
# <a name="ienumstring_next_wic_proxy-function"></a><span data-ttu-id="32f86-103">\_ \_ Funzione proxy WIC successiva IEnumString \_</span><span class="sxs-lookup"><span data-stu-id="32f86-103">IEnumString\_Next\_WIC\_Proxy function</span></span>

<span data-ttu-id="32f86-104">Funzione proxy di Windows Imaging Component (WIC) per IEnumString:: Next.</span><span class="sxs-lookup"><span data-stu-id="32f86-104">Windows Imaging Component (WIC) proxy function for IEnumString::Next.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f86-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32f86-105">Syntax</span></span>


```C++
HRESULT IEnumString_Next_WIC_Proxy(
  _In_ IEnumString *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="32f86-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32f86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f86-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32f86-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f86-108">Tipo: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="32f86-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="32f86-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="32f86-109">PARAMDESC</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f86-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32f86-110">Return value</span></span>

<span data-ttu-id="32f86-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="32f86-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="32f86-112">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="32f86-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32f86-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32f86-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="32f86-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="32f86-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="32f86-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32f86-115">Requirements</span></span>



| <span data-ttu-id="32f86-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f86-116">Requirement</span></span> | <span data-ttu-id="32f86-117">Valore</span><span class="sxs-lookup"><span data-stu-id="32f86-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f86-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32f86-119">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32f86-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="32f86-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32f86-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32f86-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="32f86-122">DLL</span><span class="sxs-lookup"><span data-stu-id="32f86-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f86-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32f86-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




