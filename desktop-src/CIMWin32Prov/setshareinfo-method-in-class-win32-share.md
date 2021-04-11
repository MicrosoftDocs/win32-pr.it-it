---
description: SetShareInfo&\# 8194; Il metodo della classe WMI imposta i parametri di una risorsa condivisa.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Metodo SetShareInfo della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225789"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="e9f50-103">Metodo SetShareInfo della classe di \_ condivisione Win32</span><span class="sxs-lookup"><span data-stu-id="e9f50-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="e9f50-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** imposta i parametri di una risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9f50-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="e9f50-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e9f50-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9f50-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e9f50-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f50-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f50-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="e9f50-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9f50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f50-109">*MaximumAllowed* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9f50-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f50-110">Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="e9f50-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="e9f50-111">Esempio: 10.</span><span class="sxs-lookup"><span data-stu-id="e9f50-111">Example: 10.</span></span> <span data-ttu-id="e9f50-112">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9f50-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e9f50-113">*Descrizione* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9f50-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f50-114">Commento facoltativo per descrivere la risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9f50-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="e9f50-115">*Accesso* \[ a in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9f50-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f50-116">Descrittore di sicurezza per le autorizzazioni a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="e9f50-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="e9f50-117">Un descrittore di sicurezza contiene informazioni sulle funzionalità di autorizzazione, proprietario e accesso della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e9f50-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="e9f50-118">Per ulteriori informazioni, vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="e9f50-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f50-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9f50-119">Return value</span></span>

<span data-ttu-id="e9f50-120">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="e9f50-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e9f50-121">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="e9f50-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-122">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="e9f50-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-123">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="e9f50-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-124">**Nome non valido** (9)</span><span class="sxs-lookup"><span data-stu-id="e9f50-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-125">**Livello non valido** (10)</span><span class="sxs-lookup"><span data-stu-id="e9f50-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-126">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="e9f50-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-127">**Condivisione duplicata** (22)</span><span class="sxs-lookup"><span data-stu-id="e9f50-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-128">**Percorso reindirizzato** (23)</span><span class="sxs-lookup"><span data-stu-id="e9f50-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-129">**Dispositivo o directory sconosciuta** (24)</span><span class="sxs-lookup"><span data-stu-id="e9f50-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-130">**Nome NET non trovato** (25)</span><span class="sxs-lookup"><span data-stu-id="e9f50-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="e9f50-131">**Altro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="e9f50-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f50-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f50-132">Remarks</span></span>

<span data-ttu-id="e9f50-133">Il metodo **SetShareInfo** è un metodo di oggetto dinamico e viene usato su un'occorrenza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e9f50-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="e9f50-134">Solo i membri del gruppo locale Administrators o account Operators o quelli con appartenenza a gruppi di operatori di comunicazione, stampa o server possono eseguire correttamente **SetShareInfo**.</span><span class="sxs-lookup"><span data-stu-id="e9f50-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="e9f50-135">L'operatore Print può impostare solo le code della stampante.</span><span class="sxs-lookup"><span data-stu-id="e9f50-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="e9f50-136">L'operatore di comunicazione può impostare solo le code del dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="e9f50-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="e9f50-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="e9f50-137">Examples</span></span>

<span data-ttu-id="e9f50-138">L'esempio di PowerShell seguente aggiorna il nome della condivisione **newShare** .</span><span class="sxs-lookup"><span data-stu-id="e9f50-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="e9f50-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f50-139">Requirements</span></span>



| <span data-ttu-id="e9f50-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f50-140">Requirement</span></span> | <span data-ttu-id="e9f50-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f50-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f50-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f50-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f50-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9f50-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9f50-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f50-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f50-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9f50-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9f50-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9f50-146">Namespace</span></span><br/>                | <span data-ttu-id="e9f50-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e9f50-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9f50-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e9f50-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9f50-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9f50-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9f50-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f50-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f50-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9f50-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f50-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f50-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9f50-153">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9f50-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9f50-154">**\_Condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="e9f50-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

