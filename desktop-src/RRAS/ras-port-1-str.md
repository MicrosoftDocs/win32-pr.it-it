---
title: Struttura RAS_PORT_1 (rassapi. h)
description: La \_ struttura della porta RAS \_ 1 contiene informazioni su una porta RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS struttura RAS_PORT_1
- RAS puntatore alla struttura PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301755"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="f9be9-105">\_Struttura porta RAS \_ 1</span><span class="sxs-lookup"><span data-stu-id="f9be9-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="f9be9-106">\[Questa versione della struttura **della \_ porta RAS \_ 1** non è supportata a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9be9-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="f9be9-107">Usare invece la [**\_ porta RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) più recente definita in mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="f9be9-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="f9be9-108">La struttura della **\_ porta RAS \_ 1** contiene informazioni su una porta RAS.</span><span class="sxs-lookup"><span data-stu-id="f9be9-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9be9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9be9-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="f9be9-110">Members</span><span class="sxs-lookup"><span data-stu-id="f9be9-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9be9-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="f9be9-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-112">Specifica una struttura di [**\_ porta RAS \_ 0**](ras-port-0-str.md) che contiene informazioni sulla porta, ad esempio il nome della porta, il nome dell'utente remoto connesso alla porta e così via.</span><span class="sxs-lookup"><span data-stu-id="f9be9-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f9be9-113">**LineCondition**</span><span class="sxs-lookup"><span data-stu-id="f9be9-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-114">Specifica lo stato della porta.</span><span class="sxs-lookup"><span data-stu-id="f9be9-114">Specifies the state of the port.</span></span> <span data-ttu-id="f9be9-115">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f9be9-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="f9be9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f9be9-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="f9be9-117">Significato</span><span class="sxs-lookup"><span data-stu-id="f9be9-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="f9be9-118"><dt>**\_porta RAS \_ non \_ operativa**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="f9be9-119">La porta non è operativa.</span><span class="sxs-lookup"><span data-stu-id="f9be9-119">The port is not operational.</span></span> <span data-ttu-id="f9be9-120">Controllare se nel registro eventi sono presenti errori segnalati dal server.</span><span class="sxs-lookup"><span data-stu-id="f9be9-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="f9be9-121"><dt>**\_porta RAS \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="f9be9-122">La porta è attualmente disconnessa.</span><span class="sxs-lookup"><span data-stu-id="f9be9-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="f9be9-123"><dt>**\_chiamata della porta RAS \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="f9be9-124">Il server RAS sta richiamando il client RAS.</span><span class="sxs-lookup"><span data-stu-id="f9be9-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="f9be9-125"><dt>**\_ascolto porta \_ RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="f9be9-126">La porta è in attesa che un client chiami.</span><span class="sxs-lookup"><span data-stu-id="f9be9-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="f9be9-127"><dt>**\_autenticazione porta \_ RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="f9be9-128">Il server è in fase di autenticazione del client remoto.</span><span class="sxs-lookup"><span data-stu-id="f9be9-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="f9be9-129"><dt>**\_porta RAS \_ autenticata**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="f9be9-130">Il client remoto è ora autenticato.</span><span class="sxs-lookup"><span data-stu-id="f9be9-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="f9be9-131"><dt>**\_ \_ inizializzazione porta RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="f9be9-132">Il dispositivo collegato alla porta verrà inizializzato.</span><span class="sxs-lookup"><span data-stu-id="f9be9-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="f9be9-133">Lo stato della porta passerà alla porta RAS \_ in \_ ascolto quando l'inizializzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f9be9-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f9be9-134">**HardwareCondition**</span><span class="sxs-lookup"><span data-stu-id="f9be9-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-135">Specifica uno dei valori seguenti per indicare lo stato del dispositivo collegato alla porta.</span><span class="sxs-lookup"><span data-stu-id="f9be9-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="f9be9-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f9be9-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="f9be9-137">Significato</span><span class="sxs-lookup"><span data-stu-id="f9be9-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="f9be9-138"><dt>**\_modem RAS \_ operativo**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="f9be9-139">Il modem collegato a questa porta è operativo ed è pronto per ricevere le chiamate del client.</span><span class="sxs-lookup"><span data-stu-id="f9be9-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="f9be9-140"><dt>**\_ \_ errore hardware del modem RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="f9be9-141">Il modem collegato a questa porta presenta un problema hardware.</span><span class="sxs-lookup"><span data-stu-id="f9be9-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="f9be9-142">**LineSpeed**</span><span class="sxs-lookup"><span data-stu-id="f9be9-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-143">Specifica la velocità, in bit al secondo, con cui il computer può comunicare con la porta.</span><span class="sxs-lookup"><span data-stu-id="f9be9-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="f9be9-144">**NumStatistics**</span><span class="sxs-lookup"><span data-stu-id="f9be9-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-145">Questo membro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f9be9-145">This member is not used.</span></span> <span data-ttu-id="f9be9-146">Le funzioni di amministrazione RAS, ad esempio la funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , utilizzano la struttura delle [**\_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) per restituire le statistiche sulle porte.</span><span class="sxs-lookup"><span data-stu-id="f9be9-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="f9be9-147">**NumMediaParms**</span><span class="sxs-lookup"><span data-stu-id="f9be9-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-148">Specifica il numero di parametri specifici del supporto per questa porta.</span><span class="sxs-lookup"><span data-stu-id="f9be9-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="f9be9-149">Per i supporti seriali si tratta in genere del numero di valori visualizzati nel file di SERIAL.INI.</span><span class="sxs-lookup"><span data-stu-id="f9be9-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="f9be9-150">**SizeMediaParms**</span><span class="sxs-lookup"><span data-stu-id="f9be9-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-151">Specifica la dimensione, in byte, del buffer necessario per tutti i parametri specifici del supporto.</span><span class="sxs-lookup"><span data-stu-id="f9be9-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="f9be9-152">La funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) restituisce un buffer che contiene una matrice di strutture di [**\_ parametri RAS**](ras-parameters-str.md) con i parametri e i valori del supporto per la porta.</span><span class="sxs-lookup"><span data-stu-id="f9be9-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="f9be9-153">**ProjResult**</span><span class="sxs-lookup"><span data-stu-id="f9be9-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="f9be9-154">Struttura [**di \_ \_ \_ Risultati della proiezione PPP RAS**](ras-ppp-projection-result-str.md) che specifica le informazioni sulla proiezione PPP per questa porta.</span><span class="sxs-lookup"><span data-stu-id="f9be9-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="f9be9-155">Questa struttura fornisce informazioni per ogni protocollo negoziato quando un client RAS si connette a un server.</span><span class="sxs-lookup"><span data-stu-id="f9be9-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9be9-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9be9-156">Requirements</span></span>



| <span data-ttu-id="f9be9-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9be9-157">Requirement</span></span> | <span data-ttu-id="f9be9-158">Valore</span><span class="sxs-lookup"><span data-stu-id="f9be9-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9be9-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9be9-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f9be9-160">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f9be9-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f9be9-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9be9-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f9be9-162">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f9be9-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f9be9-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f9be9-163">End of client support</span></span><br/>    | <span data-ttu-id="f9be9-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f9be9-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="f9be9-165">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f9be9-165">End of server support</span></span><br/>    | <span data-ttu-id="f9be9-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9be9-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="f9be9-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9be9-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9be9-168"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9be9-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9be9-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9be9-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9be9-170">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="f9be9-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="f9be9-171">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="f9be9-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="f9be9-172">**\_parametri RAS**</span><span class="sxs-lookup"><span data-stu-id="f9be9-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="f9be9-173">**\_Porta RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="f9be9-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="f9be9-174">**\_statistiche porta \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="f9be9-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="f9be9-175">**\_risultato della \_ proiezione \_ PPP RAS**</span><span class="sxs-lookup"><span data-stu-id="f9be9-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="f9be9-176">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="f9be9-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="f9be9-177">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="f9be9-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="f9be9-178">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f9be9-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





