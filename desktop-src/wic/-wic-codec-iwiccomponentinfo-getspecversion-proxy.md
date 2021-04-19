---
description: Funzione proxy per il metodo GetSpecVersion.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: Funzione IWICComponentInfo_GetSpecVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319559"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="d3ea2-103">IWICComponentInfo \_ GetSpecVersion- \_ funzione proxy</span><span class="sxs-lookup"><span data-stu-id="d3ea2-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="d3ea2-104">Funzione proxy per il metodo [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .</span><span class="sxs-lookup"><span data-stu-id="d3ea2-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ea2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3ea2-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="d3ea2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3ea2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ea2-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3ea2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ea2-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="d3ea2-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="d3ea2-109">Puntatore a questo oggetto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="d3ea2-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d3ea2-110">*cchSpecVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3ea2-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ea2-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d3ea2-111">Type: **UINT**</span></span>

<span data-ttu-id="d3ea2-112">Dimensioni del buffer *wzSpecVersion* .</span><span class="sxs-lookup"><span data-stu-id="d3ea2-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d3ea2-113">*wzSpecVersion* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d3ea2-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ea2-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d3ea2-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="d3ea2-115">Quando termina, questo metodo contiene una stringa invarient delle impostazioni cultura della versione specifica del componente.</span><span class="sxs-lookup"><span data-stu-id="d3ea2-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="d3ea2-116">Il formato della versione è NN. NN. nn. NN.</span><span class="sxs-lookup"><span data-stu-id="d3ea2-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="d3ea2-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d3ea2-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ea2-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="d3ea2-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="d3ea2-119">Puntatore che riceve la lunghezza effettiva della versione della specifica del componente.</span><span class="sxs-lookup"><span data-stu-id="d3ea2-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ea2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3ea2-120">Return value</span></span>

<span data-ttu-id="d3ea2-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d3ea2-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d3ea2-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3ea2-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3ea2-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3ea2-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3ea2-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d3ea2-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ea2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3ea2-125">Requirements</span></span>



| <span data-ttu-id="d3ea2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ea2-126">Requirement</span></span> | <span data-ttu-id="d3ea2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d3ea2-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ea2-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3ea2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ea2-129">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3ea2-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d3ea2-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3ea2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ea2-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3ea2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d3ea2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d3ea2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3ea2-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3ea2-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




