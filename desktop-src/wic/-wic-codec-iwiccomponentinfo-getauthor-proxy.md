---
description: Funzione proxy per il metodo GetAuthor.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: Funzione IWICComponentInfo_GetAuthor_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317264"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a><span data-ttu-id="f6064-103">\_Funzione proxy IWICComponentInfo GetAuthor \_</span><span class="sxs-lookup"><span data-stu-id="f6064-103">IWICComponentInfo\_GetAuthor\_Proxy function</span></span>

<span data-ttu-id="f6064-104">Funzione proxy per il metodo [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) .</span><span class="sxs-lookup"><span data-stu-id="f6064-104">Proxy function for the [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6064-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6064-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="f6064-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6064-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6064-107">*Questa \_ PTR* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6064-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6064-108">Tipo: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f6064-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="f6064-109">Puntatore a questo oggetto [_ *IWICComponentInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="f6064-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="f6064-110">*cchAuthor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6064-110">*cchAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6064-111">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f6064-111">Type: **UINT**</span></span>

<span data-ttu-id="f6064-112">Dimensioni del buffer *wzAuthor* .</span><span class="sxs-lookup"><span data-stu-id="f6064-112">The size of the *wzAuthor* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f6064-113">*wzAuthor* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f6064-113">*wzAuthor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6064-114">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="f6064-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="f6064-115">Puntatore che riceve il nome dell'autore del componente.</span><span class="sxs-lookup"><span data-stu-id="f6064-115">A pointer that receives the name of the component's author.</span></span>

<span data-ttu-id="f6064-116">La stringa restituita è specifica delle impostazioni locali, 1033 per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f6064-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="f6064-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f6064-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6064-118">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="f6064-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="f6064-119">Puntatore che riceve la lunghezza effettiva del nome degli autori del componente.</span><span class="sxs-lookup"><span data-stu-id="f6064-119">A pointer that receives the actual length of the component's authors name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6064-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6064-120">Return value</span></span>

<span data-ttu-id="f6064-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f6064-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f6064-122">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f6064-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6064-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6064-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6064-124">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="f6064-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f6064-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6064-125">Requirements</span></span>



| <span data-ttu-id="f6064-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6064-126">Requirement</span></span> | <span data-ttu-id="f6064-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f6064-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6064-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6064-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f6064-129">Windows XP con SP2, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6064-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f6064-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6064-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f6064-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6064-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f6064-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f6064-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6064-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6064-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




