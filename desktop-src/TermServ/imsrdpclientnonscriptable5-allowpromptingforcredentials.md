---
title: Proprietà AllowPromptingForCredentials di IMsRdpClientNonScriptable5
description: Specifica se il controllo ActiveX Desktop remoto può richiedere le credenziali all'utente.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AllowPromptingForCredentials
- Servizi Desktop remoto proprietà AllowPromptingForCredentials, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302742"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a><span data-ttu-id="d3a49-106">Proprietà IMsRdpClientNonScriptable5:: AllowPromptingForCredentials</span><span class="sxs-lookup"><span data-stu-id="d3a49-106">IMsRdpClientNonScriptable5::AllowPromptingForCredentials property</span></span>

<span data-ttu-id="d3a49-107">Specifica se il controllo ActiveX Desktop remoto può richiedere le credenziali all'utente.</span><span class="sxs-lookup"><span data-stu-id="d3a49-107">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span> <span data-ttu-id="d3a49-108">Se questa proprietà contiene la **variante \_ true**, all'utente possono essere richieste le credenziali.</span><span class="sxs-lookup"><span data-stu-id="d3a49-108">If this property contains **VARIANT\_TRUE**, the user can be prompted for credentials.</span></span> <span data-ttu-id="d3a49-109">Se questa proprietà contiene il valore **Variant \_ false**, all'utente non verrà richiesto di immettere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="d3a49-109">If this property contains **VARIANT\_FALSE**, the user cannot be prompted for credentials.</span></span>

<span data-ttu-id="d3a49-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d3a49-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a49-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3a49-111">Syntax</span></span>


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a><span data-ttu-id="d3a49-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d3a49-112">Property value</span></span>

<span data-ttu-id="d3a49-113">Specifica il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3a49-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a49-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3a49-114">Requirements</span></span>



| <span data-ttu-id="d3a49-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a49-115">Requirement</span></span> | <span data-ttu-id="d3a49-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d3a49-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a49-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a49-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a49-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3a49-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3a49-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a49-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a49-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d3a49-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="d3a49-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d3a49-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3a49-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3a49-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d3a49-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d3a49-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3a49-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3a49-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d3a49-125">IID</span><span class="sxs-lookup"><span data-stu-id="d3a49-125">IID</span></span><br/>                      | <span data-ttu-id="d3a49-126">IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="d3a49-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3a49-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3a49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a49-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d3a49-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





