---
title: Proprietà EnableSuperPan di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore booleano che indica se SuperPan è abilitato o disabilitato.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableSuperPan
- Servizi Desktop remoto proprietà EnableSuperPan, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableSuperPan
- Servizi Desktop remoto proprietà EnableSuperPan, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742135"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="63e30-108">Proprietà IMsRdpClientAdvancedSettings7:: EnableSuperPan</span><span class="sxs-lookup"><span data-stu-id="63e30-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="63e30-109">Specifica o recupera un valore booleano che indica se SuperPan è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="63e30-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="63e30-110">SuperPan è una funzionalità che consente a un utente di spostarsi facilmente in un desktop remoto in modalità schermo intero, quando le dimensioni del desktop remoto sono maggiori delle dimensioni della finestra client corrente.</span><span class="sxs-lookup"><span data-stu-id="63e30-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="63e30-111">Anziché utilizzare le barre di scorrimento per spostarsi sul desktop, l'utente può puntare al bordo della finestra e il desktop remoto scorre automaticamente in tale direzione.</span><span class="sxs-lookup"><span data-stu-id="63e30-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="63e30-112">SuperPan non supporta più di un monitor.</span><span class="sxs-lookup"><span data-stu-id="63e30-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="63e30-113">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="63e30-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e30-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63e30-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="63e30-115">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="63e30-115">Property value</span></span>

<span data-ttu-id="63e30-116">Valore **\_ bool Variant** che specifica se SuperPan è abilitato.</span><span class="sxs-lookup"><span data-stu-id="63e30-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="63e30-117">Il valore **Variant \_ true** specifica che SuperPan è abilitato.</span><span class="sxs-lookup"><span data-stu-id="63e30-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e30-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63e30-118">Requirements</span></span>



| <span data-ttu-id="63e30-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e30-119">Requirement</span></span> | <span data-ttu-id="63e30-120">Valore</span><span class="sxs-lookup"><span data-stu-id="63e30-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e30-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63e30-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63e30-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63e30-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="63e30-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63e30-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63e30-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63e30-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="63e30-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="63e30-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="63e30-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e30-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="63e30-127">DLL</span><span class="sxs-lookup"><span data-stu-id="63e30-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e30-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e30-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="63e30-129">IID</span><span class="sxs-lookup"><span data-stu-id="63e30-129">IID</span></span><br/>                      | <span data-ttu-id="63e30-130">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="63e30-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63e30-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63e30-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e30-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="63e30-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="63e30-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="63e30-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





