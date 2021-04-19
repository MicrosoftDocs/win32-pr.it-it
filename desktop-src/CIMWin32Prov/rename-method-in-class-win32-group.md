---
description: Consente di modificare il nome del gruppo.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304436"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="3a653-103">Rinominare il metodo della \_ classe del gruppo Win32</span><span class="sxs-lookup"><span data-stu-id="3a653-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="3a653-104">Il metodo **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) consente di modificare il nome del gruppo.</span><span class="sxs-lookup"><span data-stu-id="3a653-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="3a653-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3a653-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3a653-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3a653-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a653-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a653-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="3a653-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a653-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a653-109">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a653-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a653-110">Nome dell'account utente di Windows nel dominio specificato dalla proprietà del **dominio** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="3a653-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a653-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a653-111">Return value</span></span>

<span data-ttu-id="3a653-112">Il metodo **Rename** può restituire i codici di errore elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="3a653-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="3a653-113">Per i valori integer diversi da quelli elencati, fare riferimento ai [ \_ codici restituiti di WMI](/windows/desktop/WmiSdk/wmi-return-codes).</span><span class="sxs-lookup"><span data-stu-id="3a653-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3a653-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="3a653-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-115">0</span><span class="sxs-lookup"><span data-stu-id="3a653-115">0</span></span>

<span data-ttu-id="3a653-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3a653-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3a653-117">**Istanza non trovata**</span><span class="sxs-lookup"><span data-stu-id="3a653-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-118">1</span><span class="sxs-lookup"><span data-stu-id="3a653-118">1</span></span>

</dd> <dt>

<span data-ttu-id="3a653-119">**Istanza obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="3a653-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-120">2</span><span class="sxs-lookup"><span data-stu-id="3a653-120">2</span></span>

</dd> <dt>

<span data-ttu-id="3a653-121">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="3a653-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-122">3</span><span class="sxs-lookup"><span data-stu-id="3a653-122">3</span></span>

</dd> <dt>

<span data-ttu-id="3a653-123">**Il gruppo non è stato trovato**</span><span class="sxs-lookup"><span data-stu-id="3a653-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-124">4</span><span class="sxs-lookup"><span data-stu-id="3a653-124">4</span></span>

</dd> <dt>

<span data-ttu-id="3a653-125">**Dominio non trovato**</span><span class="sxs-lookup"><span data-stu-id="3a653-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-126">5</span><span class="sxs-lookup"><span data-stu-id="3a653-126">5</span></span>

</dd> <dt>

<span data-ttu-id="3a653-127">**L'operazione è consentita solo sul controller di dominio primario del dominio**</span><span class="sxs-lookup"><span data-stu-id="3a653-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-128">6</span><span class="sxs-lookup"><span data-stu-id="3a653-128">6</span></span>

</dd> <dt>

<span data-ttu-id="3a653-129">**Operazione non consentita per gruppi speciali specificati. utente, amministratore, locale o Guest.**</span><span class="sxs-lookup"><span data-stu-id="3a653-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-130">7</span><span class="sxs-lookup"><span data-stu-id="3a653-130">7</span></span>

</dd> <dt>

<span data-ttu-id="3a653-131">**Altro errore API**</span><span class="sxs-lookup"><span data-stu-id="3a653-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-132">8</span><span class="sxs-lookup"><span data-stu-id="3a653-132">8</span></span>

</dd> <dt>

<span data-ttu-id="3a653-133">**Errore interno**</span><span class="sxs-lookup"><span data-stu-id="3a653-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="3a653-134">9</span><span class="sxs-lookup"><span data-stu-id="3a653-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a653-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a653-135">Requirements</span></span>



| <span data-ttu-id="3a653-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a653-136">Requirement</span></span> | <span data-ttu-id="3a653-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3a653-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a653-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a653-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3a653-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a653-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a653-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a653-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3a653-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a653-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a653-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a653-142">Namespace</span></span><br/>                | <span data-ttu-id="3a653-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3a653-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a653-144">MOF</span><span class="sxs-lookup"><span data-stu-id="3a653-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a653-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a653-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a653-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3a653-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a653-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a653-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a653-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a653-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a653-149">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a653-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3a653-150">**\_Gruppo Win32**</span><span class="sxs-lookup"><span data-stu-id="3a653-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="3a653-151">**\_LogicalFileSecuritySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3a653-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

