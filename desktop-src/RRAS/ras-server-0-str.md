---
title: Struttura RAS_SERVER_0 (rassapi. h)
description: La \_ struttura del server RAS \_ 0 viene utilizzata dalla funzione RasAdminServerGetInfo per restituire informazioni sulle porte configurate in un server RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS struttura RAS_SERVER_0
- RAS puntatore alla struttura PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302186"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="9f8ba-105">\_Struttura server RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="9f8ba-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="9f8ba-106">\[La struttura del **\_ server RAS \_ 0** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="9f8ba-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="9f8ba-107">La struttura del **\_ server RAS \_ 0** viene utilizzata dalla funzione [**RasAdminServerGetInfo**](rasadminservergetinfo.md) per restituire informazioni sulle porte configurate in un server RAS.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f8ba-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="9f8ba-109">Members</span><span class="sxs-lookup"><span data-stu-id="9f8ba-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f8ba-110">**TotalPorts**</span><span class="sxs-lookup"><span data-stu-id="9f8ba-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="9f8ba-111">Specifica il numero totale di porte configurate nel server RAS disponibili per la connessione dei client remoti.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="9f8ba-112">Se, ad esempio, il numero totale di porte configurate per la connessione a un server è quattro, ma una delle porte è attualmente in uso per la connessione, **TotalPorts** è tre.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="9f8ba-113">**PortsInUse**</span><span class="sxs-lookup"><span data-stu-id="9f8ba-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="9f8ba-114">Specifica il numero di porte attualmente utilizzate dai client remoti.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="9f8ba-115">**RasVersion**</span><span class="sxs-lookup"><span data-stu-id="9f8ba-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9f8ba-116">Specifica la versione del server RAS.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="9f8ba-117">Usare queste informazioni per eseguire un'azione specifica della versione.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="9f8ba-118">Questo membro è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-118">This member is one of the following values.</span></span>



| <span data-ttu-id="9f8ba-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9f8ba-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="9f8ba-120">Significato</span><span class="sxs-lookup"><span data-stu-id="9f8ba-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="9f8ba-121"><dt>**RASDOWNLEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="9f8ba-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="9f8ba-122">Indica un server RAS della versione 1,0 di LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="9f8ba-123"><dt>**RASADMIN \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="9f8ba-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="9f8ba-124">Indica un server o un client RAS Windows NT Server 3,51 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="9f8ba-125"><dt>**RASADMIN \_ corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="9f8ba-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="9f8ba-126">Indica un server o un client RAS Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="9f8ba-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f8ba-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f8ba-127">Requirements</span></span>



| <span data-ttu-id="9f8ba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f8ba-128">Requirement</span></span> | <span data-ttu-id="9f8ba-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9f8ba-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8ba-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f8ba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9f8ba-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f8ba-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9f8ba-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f8ba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9f8ba-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f8ba-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9f8ba-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9f8ba-134">End of client support</span></span><br/>    | <span data-ttu-id="9f8ba-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f8ba-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="9f8ba-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9f8ba-136">End of server support</span></span><br/>    | <span data-ttu-id="9f8ba-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f8ba-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="9f8ba-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f8ba-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f8ba-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f8ba-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f8ba-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f8ba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8ba-141">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="9f8ba-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="9f8ba-142">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="9f8ba-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="9f8ba-143">**RasAdminServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9f8ba-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





