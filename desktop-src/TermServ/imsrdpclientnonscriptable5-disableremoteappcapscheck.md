---
title: Proprietà DisableRemoteAppCapsCheck di IMsRdpClientNonScriptable5
description: Specifica se il controllo ActiveX Desktop remoto non deve controllare il server per le funzionalità di RemoteApp.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisableRemoteAppCapsCheck
- Servizi Desktop remoto proprietà DisableRemoteAppCapsCheck, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà DisableRemoteAppCapsCheck
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479288"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="a2228-106">IMsRdpClientNonScriptable5::D Proprietà isableRemoteAppCapsCheck</span><span class="sxs-lookup"><span data-stu-id="a2228-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="a2228-107">Specifica se il controllo ActiveX Desktop remoto non deve controllare il server per le funzionalità di RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a2228-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="a2228-108">Se questa proprietà contiene la **variante \_ true**, il controllo non deve controllare il server per le funzionalità di RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a2228-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="a2228-109">Se questa proprietà contiene la **variante \_ false**, il controllo può controllare il server per le funzionalità di RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a2228-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="a2228-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a2228-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2228-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2228-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="a2228-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a2228-112">Property value</span></span>

<span data-ttu-id="a2228-113">Specifica il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a2228-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2228-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2228-114">Requirements</span></span>



| <span data-ttu-id="a2228-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2228-115">Requirement</span></span> | <span data-ttu-id="a2228-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a2228-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2228-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2228-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2228-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2228-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2228-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2228-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2228-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2228-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="a2228-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a2228-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2228-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2228-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a2228-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a2228-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2228-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2228-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a2228-125">IID</span><span class="sxs-lookup"><span data-stu-id="a2228-125">IID</span></span><br/>                      | <span data-ttu-id="a2228-126">IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="a2228-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2228-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2228-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2228-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a2228-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





