---
description: Funzione proxy per il metodo GetFriendlyName.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: Funzione IWICComponentInfo_GetFriendlyName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314889"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="887df-103">IWICComponentInfo \_ funzione proxy GetFriendlyName \_</span><span class="sxs-lookup"><span data-stu-id="887df-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="887df-104">Funzione proxy per il metodo [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .</span><span class="sxs-lookup"><span data-stu-id="887df-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="887df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="887df-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="887df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="887df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="887df-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="887df-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887df-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="887df-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="887df-109">Puntatore a questo oggetto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="887df-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="887df-110">*cchFriendlyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="887df-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="887df-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="887df-111">Type: **UINT**</span></span>

<span data-ttu-id="887df-112">Dimensioni del buffer *wzFriendlyName* .</span><span class="sxs-lookup"><span data-stu-id="887df-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="887df-113">*wzFriendlyName* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="887df-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="887df-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="887df-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="887df-115">Puntatore che riceve il nome descrittivo del componente.</span><span class="sxs-lookup"><span data-stu-id="887df-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="887df-116">La stringa restituita è specifica delle impostazioni locali, 1033 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="887df-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="887df-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="887df-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="887df-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="887df-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="887df-119">Puntatore che riceve la lunghezza effettiva del nome descrittivo del componente.</span><span class="sxs-lookup"><span data-stu-id="887df-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="887df-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="887df-120">Return value</span></span>

<span data-ttu-id="887df-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="887df-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="887df-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="887df-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="887df-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="887df-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="887df-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="887df-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="887df-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="887df-125">Requirements</span></span>



| <span data-ttu-id="887df-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="887df-126">Requirement</span></span> | <span data-ttu-id="887df-127">Valore</span><span class="sxs-lookup"><span data-stu-id="887df-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887df-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887df-128">Minimum supported client</span></span><br/> | <span data-ttu-id="887df-129">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="887df-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="887df-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887df-130">Minimum supported server</span></span><br/> | <span data-ttu-id="887df-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="887df-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="887df-132">DLL</span><span class="sxs-lookup"><span data-stu-id="887df-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887df-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="887df-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




