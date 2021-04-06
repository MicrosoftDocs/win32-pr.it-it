---
title: Metodo RestoreDefaults della classe Win32_TSPermissionsSetting (Netfw. h)
description: Ripristina i valori predefiniti del set di autorizzazioni per il terminale.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo RestoreDefaults
- Metodo RestoreDefaults Servizi Desktop remoto, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Servizi Desktop remoto, Metodo RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873617"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="516e7-106">Metodo RestoreDefaults della \_ classe TSPermissionsSetting Win32</span><span class="sxs-lookup"><span data-stu-id="516e7-106">RestoreDefaults method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="516e7-107">Il metodo **RestoreDefaults** Ripristina i valori predefiniti del set di autorizzazioni per il terminale.</span><span class="sxs-lookup"><span data-stu-id="516e7-107">The **RestoreDefaults** method restores the default permission set values for the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="516e7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="516e7-108">Syntax</span></span>


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a><span data-ttu-id="516e7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="516e7-109">Parameters</span></span>

<span data-ttu-id="516e7-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="516e7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="516e7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="516e7-111">Return value</span></span>

<span data-ttu-id="516e7-112">Restituisce l'esito positivo, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="516e7-112">Returns Success on success, otherwise Failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="516e7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="516e7-113">Remarks</span></span>

<span data-ttu-id="516e7-114">Le autorizzazioni predefinite sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="516e7-114">Default permissions are the following:</span></span>

-   <span data-ttu-id="516e7-115">Gli account amministratori, di sistema e di Desktop remoto Assistant sono dotati di [autorizzazioni di Servizi Desktop remoto](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="516e7-115">The Administrators, System, and Remote Desktop Help Assistant accounts have all [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>
-   <span data-ttu-id="516e7-116">L'account utenti Desktop remoto dispone dell'autorizzazione di accesso, connessione, informazioni sulle query e invio del messaggio.</span><span class="sxs-lookup"><span data-stu-id="516e7-116">The Remote Desktop Users account has Logon, Connect, Query Information, and Send Message permission.</span></span>
-   <span data-ttu-id="516e7-117">Gli account servizio locale e servizio di rete dispongono di informazioni sulle query e dell'autorizzazione Invia messaggio.</span><span class="sxs-lookup"><span data-stu-id="516e7-117">The Local Service and Network Service accounts have Query Information, and Send Message permission.</span></span>

<span data-ttu-id="516e7-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="516e7-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="516e7-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="516e7-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="516e7-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="516e7-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="516e7-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="516e7-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="516e7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="516e7-122">Requirements</span></span>



| <span data-ttu-id="516e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="516e7-123">Requirement</span></span> | <span data-ttu-id="516e7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="516e7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516e7-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="516e7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="516e7-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="516e7-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="516e7-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="516e7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="516e7-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="516e7-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="516e7-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="516e7-129">Namespace</span></span><br/>                | <span data-ttu-id="516e7-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="516e7-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="516e7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="516e7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="516e7-132"><dt>Netfw. h</dt></span><span class="sxs-lookup"><span data-stu-id="516e7-132"><dt>Netfw.h</dt></span></span> </dl>      |
| <span data-ttu-id="516e7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="516e7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="516e7-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="516e7-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="516e7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="516e7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="516e7-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="516e7-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516e7-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="516e7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516e7-138">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="516e7-138">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

