---
title: Proprietà EnableCredSspSupport di IMsRdpClientAdvancedSettings6
description: Specifica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517757"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="8e61a-110">Proprietà IMsRdpClientAdvancedSettings6:: EnableCredSspSupport</span><span class="sxs-lookup"><span data-stu-id="8e61a-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="8e61a-111">Specifica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e61a-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="8e61a-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8e61a-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e61a-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e61a-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="8e61a-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8e61a-114">Property value</span></span>

<span data-ttu-id="8e61a-115">Specifica se CredSSP è abilitato per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="8e61a-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="8e61a-116">Impostare su **Variant \_ true** per abilitare CredSSP o **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8e61a-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e61a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e61a-117">Remarks</span></span>

<span data-ttu-id="8e61a-118">Questa proprietà è supportata solo dai client Connessione Desktop remoto 6,1 e 7,0.</span><span class="sxs-lookup"><span data-stu-id="8e61a-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e61a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e61a-119">Requirements</span></span>



| <span data-ttu-id="8e61a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e61a-120">Requirement</span></span> | <span data-ttu-id="8e61a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8e61a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e61a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e61a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e61a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e61a-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8e61a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e61a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e61a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e61a-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8e61a-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8e61a-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="8e61a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e61a-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8e61a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8e61a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e61a-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e61a-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8e61a-130">IID</span><span class="sxs-lookup"><span data-stu-id="8e61a-130">IID</span></span><br/>                      | <span data-ttu-id="8e61a-131">IID \_ IMsRdpClientAdvancedSettings6 è definito come 222c4b5d-45D9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="8e61a-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e61a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e61a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e61a-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8e61a-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8e61a-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8e61a-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8e61a-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8e61a-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





