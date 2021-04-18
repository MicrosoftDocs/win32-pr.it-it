---
title: Proprietà WorkDir di IMsTscSecuredSettings
description: Specifica la directory di lavoro del programma di avvio.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà WorkDir
- Servizi Desktop remoto proprietà WorkDir, interfaccia IMsTscSecuredSettings
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, proprietà WorkDir
- Servizi Desktop remoto proprietà WorkDir, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302610"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="1f63d-108">Proprietà IMsTscSecuredSettings:: WorkDir</span><span class="sxs-lookup"><span data-stu-id="1f63d-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="1f63d-109">Specifica la directory di lavoro del programma di avvio.</span><span class="sxs-lookup"><span data-stu-id="1f63d-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="1f63d-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1f63d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f63d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f63d-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="1f63d-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1f63d-112">Property value</span></span>

<span data-ttu-id="1f63d-113">Nuova directory di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f63d-113">The new working directory.</span></span> <span data-ttu-id="1f63d-114">La lunghezza massima di questa stringa è **Max \_ path**-1 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f63d-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f63d-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1f63d-115">Error codes</span></span>

<span data-ttu-id="1f63d-116">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1f63d-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f63d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f63d-117">Remarks</span></span>

<span data-ttu-id="1f63d-118">Per ulteriori informazioni, vedere [la pagina relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="1f63d-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="1f63d-119">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1f63d-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f63d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f63d-120">Requirements</span></span>



| <span data-ttu-id="1f63d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f63d-121">Requirement</span></span> | <span data-ttu-id="1f63d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1f63d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f63d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f63d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1f63d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f63d-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="1f63d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f63d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1f63d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f63d-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1f63d-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1f63d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f63d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f63d-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="1f63d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1f63d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f63d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f63d-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="1f63d-131">IID</span><span class="sxs-lookup"><span data-stu-id="1f63d-131">IID</span></span><br/>                      | <span data-ttu-id="1f63d-132">IID \_ IMsTscSecuredSettings è definito come c9d65442-A0F9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="1f63d-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f63d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f63d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f63d-134">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="1f63d-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1f63d-135">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="1f63d-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





