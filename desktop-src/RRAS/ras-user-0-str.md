---
title: Struttura RAS_USER_0 (rassapi. h)
description: La \_ struttura RAS user \_ 0 viene utilizzata nelle funzioni RasAdminUserSetInfo e RasAdminUserGetInfo per specificare le informazioni relative a un utente.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS struttura RAS_USER_0
- RAS puntatore alla struttura PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517716"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="1b53e-105">\_Struttura utente RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="1b53e-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="1b53e-106">\[Questa versione della struttura **RAS \_ User \_ 0** non è supportata a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b53e-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="1b53e-107">Usare invece il [**nuovo \_ utente RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) definito in mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="1b53e-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="1b53e-108">La struttura **RAS \_ User \_ 0** viene utilizzata nelle funzioni [**RasAdminUserSetInfo**](rasadminusersetinfo.md) e [**RasAdminUserGetInfo**](rasadminusergetinfo.md) per specificare le informazioni relative a un utente.</span><span class="sxs-lookup"><span data-stu-id="1b53e-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b53e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b53e-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="1b53e-110">Members</span><span class="sxs-lookup"><span data-stu-id="1b53e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b53e-111">**bfPrivilege**</span><span class="sxs-lookup"><span data-stu-id="1b53e-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="1b53e-112">Set di flag di bit che specificano i privilegi RAS dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1b53e-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="1b53e-113">Questo membro può essere una combinazione del \_ flag DialinPrivilege di RASPRIV e di uno dei flag di chiamata.</span><span class="sxs-lookup"><span data-stu-id="1b53e-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="1b53e-114">Usare la \_ maschera RASPRIV CallbackType per identificare il tipo di privilegio di callback fornito all'utente.</span><span class="sxs-lookup"><span data-stu-id="1b53e-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="1b53e-115">Vengono definiti i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="1b53e-115">The following flags are defined.</span></span>



| <span data-ttu-id="1b53e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1b53e-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="1b53e-117">Significato</span><span class="sxs-lookup"><span data-stu-id="1b53e-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="1b53e-118"><dt>**NoCallback RASPRIV \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b53e-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="1b53e-119">L'utente non dispone di alcun privilegio di chiamata.</span><span class="sxs-lookup"><span data-stu-id="1b53e-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="1b53e-120"><dt>**\_ADMINSETCALLBACK RASPRIV**</dt></span><span class="sxs-lookup"><span data-stu-id="1b53e-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="1b53e-121">L'account utente è configurato in modo che l'amministratore imposti il numero di chiamate.</span><span class="sxs-lookup"><span data-stu-id="1b53e-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="1b53e-122"><dt>**\_CALLERSETCALLBACK RASPRIV**</dt></span><span class="sxs-lookup"><span data-stu-id="1b53e-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="1b53e-123">Quando si effettua la connessione, l'utente remoto può specificare un numero di telefono di chiamata.</span><span class="sxs-lookup"><span data-stu-id="1b53e-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="1b53e-124"><dt>**\_DIALINPRIVILEGE RASPRIV**</dt></span><span class="sxs-lookup"><span data-stu-id="1b53e-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="1b53e-125">L'utente dispone delle autorizzazioni per connettersi a questo server.</span><span class="sxs-lookup"><span data-stu-id="1b53e-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="1b53e-126">Specificare uno dei flag di chiamata per la chiamata alla funzione [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1b53e-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1b53e-127">**szPhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="1b53e-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1b53e-128">Stringa Unicode con terminazione null che specifica il numero di telefono per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1b53e-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b53e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b53e-129">Requirements</span></span>



| <span data-ttu-id="1b53e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b53e-130">Requirement</span></span> | <span data-ttu-id="1b53e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1b53e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1b53e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b53e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1b53e-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1b53e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1b53e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b53e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1b53e-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1b53e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1b53e-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1b53e-136">End of client support</span></span><br/>    | <span data-ttu-id="1b53e-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b53e-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="1b53e-138">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1b53e-138">End of server support</span></span><br/>    | <span data-ttu-id="1b53e-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b53e-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="1b53e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b53e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b53e-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b53e-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b53e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b53e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b53e-143">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="1b53e-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="1b53e-144">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="1b53e-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="1b53e-145">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="1b53e-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="1b53e-146">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="1b53e-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





