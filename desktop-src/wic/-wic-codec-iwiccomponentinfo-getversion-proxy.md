---
description: Funzione proxy per il metodo GetVersion.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: Funzione IWICComponentInfo_GetVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319558"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="b2602-103">IWICComponentInfo \_ \_ funzione proxy GetVersion</span><span class="sxs-lookup"><span data-stu-id="b2602-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="b2602-104">Funzione proxy per il metodo [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .</span><span class="sxs-lookup"><span data-stu-id="b2602-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2602-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2602-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="b2602-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2602-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2602-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2602-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="b2602-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="b2602-109">Puntatore a questo oggetto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="b2602-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="b2602-110">*cchVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2602-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2602-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b2602-111">Type: **UINT**</span></span>

<span data-ttu-id="b2602-112">Dimensioni del buffer *wzVersion* .</span><span class="sxs-lookup"><span data-stu-id="b2602-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b2602-113">*wzVersion* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b2602-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2602-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="b2602-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="b2602-115">Puntatore che riceve una stringa invariante delle impostazioni cultura della versione del componente.</span><span class="sxs-lookup"><span data-stu-id="b2602-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="b2602-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2602-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2602-117">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="b2602-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="b2602-118">Puntatore che riceve la lunghezza effettiva della versione del componente.</span><span class="sxs-lookup"><span data-stu-id="b2602-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2602-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2602-119">Return value</span></span>

<span data-ttu-id="b2602-120">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b2602-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b2602-121">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b2602-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2602-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2602-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2602-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b2602-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b2602-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2602-124">Requirements</span></span>



| <span data-ttu-id="b2602-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2602-125">Requirement</span></span> | <span data-ttu-id="b2602-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b2602-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2602-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2602-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2602-128">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2602-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b2602-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2602-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2602-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2602-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b2602-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b2602-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2602-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2602-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




