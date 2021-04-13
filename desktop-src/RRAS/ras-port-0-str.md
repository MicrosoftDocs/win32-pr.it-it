---
title: Struttura RAS_PORT_0 (rassapi. h)
description: La \_ struttura della porta \_ 0 RAS contiene informazioni che descrivono una porta RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS struttura RAS_PORT_0
- RAS puntatore alla struttura PRAS_PORT_0
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517883"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="15aa4-105">\_Struttura porta RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="15aa4-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="15aa4-106">\[Questa versione della struttura **della \_ porta RAS \_ 0** non è supportata a partire da Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15aa4-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="15aa4-107">Usare invece la [**\_ porta RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) più recente definita in mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="15aa4-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="15aa4-108">La struttura della **\_ porta \_ 0 RAS** contiene informazioni che descrivono una porta RAS.</span><span class="sxs-lookup"><span data-stu-id="15aa4-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="15aa4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15aa4-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="15aa4-110">Members</span><span class="sxs-lookup"><span data-stu-id="15aa4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="15aa4-111">**wszPortName**</span><span class="sxs-lookup"><span data-stu-id="15aa4-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-112">Stringa Unicode con terminazione null che specifica il nome della porta, ad esempio "COM1".</span><span class="sxs-lookup"><span data-stu-id="15aa4-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-113">**wszDeviceType**</span><span class="sxs-lookup"><span data-stu-id="15aa4-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-114">Stringa Unicode con terminazione null che specifica il tipo del dispositivo in cui è stata effettuata la connessione, ad esempio modem o ISDN.</span><span class="sxs-lookup"><span data-stu-id="15aa4-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="15aa4-115">L'elenco dei tipi di dispositivo che potrebbero essere specificati in questo membro include tutti i tipi di dispositivo installati nel server, inclusi i dispositivi di terze parti.</span><span class="sxs-lookup"><span data-stu-id="15aa4-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-116">**wszDeviceName**</span><span class="sxs-lookup"><span data-stu-id="15aa4-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-117">Stringa Unicode con terminazione null che specifica il nome del dispositivo in cui è stata effettuata la connessione, ad esempio "Hayes 9600" o "PCIMACISDN1".</span><span class="sxs-lookup"><span data-stu-id="15aa4-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-118">**wszMediaName**</span><span class="sxs-lookup"><span data-stu-id="15aa4-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-119">Specifica una stringa Unicode con terminazione null che specifica il nome del supporto usato per la connessione, ad esempio *rasser* o *RASTAPI*.</span><span class="sxs-lookup"><span data-stu-id="15aa4-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-120">**riservati**</span><span class="sxs-lookup"><span data-stu-id="15aa4-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="15aa4-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-122">**Flag**</span><span class="sxs-lookup"><span data-stu-id="15aa4-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-123">Specifica un set di flag di bit che specificano la natura della connessione effettuata su questa porta.</span><span class="sxs-lookup"><span data-stu-id="15aa4-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="15aa4-124">Questo membro può essere una combinazione dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="15aa4-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="15aa4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="15aa4-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="15aa4-126">Significato</span><span class="sxs-lookup"><span data-stu-id="15aa4-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="15aa4-127"><dt>**GATEWAY \_ attivo**</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="15aa4-128">Se questo flag è impostato, il gateway NetBIOS è attivo sul server.</span><span class="sxs-lookup"><span data-stu-id="15aa4-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="15aa4-129"><dt>**MESSENGER \_ presente**</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="15aa4-130">Se questo flag è impostato, il servizio Messenger viene eseguito sul client remoto.</span><span class="sxs-lookup"><span data-stu-id="15aa4-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="15aa4-131"><dt>**PORTA \_ MULTIlinked**</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="15aa4-132">Se questo flag è impostato, la porta viene collegata a più porte.</span><span class="sxs-lookup"><span data-stu-id="15aa4-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="15aa4-133">Utilizzare queste informazioni per visualizzare lo stato di connessione come porta con collegamento multiplo.</span><span class="sxs-lookup"><span data-stu-id="15aa4-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="15aa4-134">Per una porta con collegamento multiplo, la struttura delle [**\_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) contiene due set di statistiche: uno solo per la porta e un altro per le porte combinate nella connessione multicollegamento.</span><span class="sxs-lookup"><span data-stu-id="15aa4-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="15aa4-135"><dt>**\_client PPP**</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="15aa4-136">Se questo flag è impostato, il client remoto si connette utilizzando PPP.</span><span class="sxs-lookup"><span data-stu-id="15aa4-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="15aa4-137">Se questo flag non è impostato, il client remoto si è connesso usando il protocollo AMB.</span><span class="sxs-lookup"><span data-stu-id="15aa4-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="15aa4-138"><dt>**\_ascolto remoto**</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="15aa4-139">Se questo flag è impostato, il parametro RemoteListen del gateway NetBIOS viene impostato su 1 sul server.</span><span class="sxs-lookup"><span data-stu-id="15aa4-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="15aa4-140"><dt>**UTENTE \_ autenticato**</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="15aa4-141">Se questo flag è impostato, un client remoto è connesso al server e l'utente è stato autenticato.</span><span class="sxs-lookup"><span data-stu-id="15aa4-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="15aa4-142">Selezionare questo flag per verificare che un client sia effettivamente connesso a una porta.</span><span class="sxs-lookup"><span data-stu-id="15aa4-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="15aa4-143">Se il MESSENGER \_ è presente, i \_ flag Active gateway e \_ ascolto remoto sono impostati, usare il servizio Messenger per inviare un messaggio amministrativo al client remoto.</span><span class="sxs-lookup"><span data-stu-id="15aa4-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="15aa4-144">Se \_ sono impostati Messenger e \_ l'ascolto remoto, ma \_ il gateway attivo non lo è, inviare i messaggi al client solo dal server RAS a cui è connesso il client.</span><span class="sxs-lookup"><span data-stu-id="15aa4-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-145">**wszUserName**</span><span class="sxs-lookup"><span data-stu-id="15aa4-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-146">Stringa Unicode con terminazione null che specifica il nome dell'utente remoto connesso a questa porta.</span><span class="sxs-lookup"><span data-stu-id="15aa4-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-147">**wszComputer**</span><span class="sxs-lookup"><span data-stu-id="15aa4-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-148">Stringa Unicode con terminazione null che specifica il nome del computer client remoto.</span><span class="sxs-lookup"><span data-stu-id="15aa4-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-149">**dwStartSessionTime**</span><span class="sxs-lookup"><span data-stu-id="15aa4-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-150">Specifica il tempo, in secondi, dal 1 gennaio 1970, che il client si è connesso al server RAS su questa porta.</span><span class="sxs-lookup"><span data-stu-id="15aa4-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="15aa4-151">Usare le funzioni temporali standard per formattare questo valore per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="15aa4-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-152">**wszLogonDomain**</span><span class="sxs-lookup"><span data-stu-id="15aa4-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-153">Specifica una stringa Unicode con terminazione null che specifica il nome del dominio in cui è stato autenticato l'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="15aa4-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="15aa4-154">Questa stringa è solo il nome di dominio, senza \\ \\ prefisso "".</span><span class="sxs-lookup"><span data-stu-id="15aa4-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="15aa4-155">**fAdvancedServer**</span><span class="sxs-lookup"><span data-stu-id="15aa4-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="15aa4-156">Specifica un flag che è diverso da zero se il server RAS associato a questa porta è un server avanzato, ad esempio Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="15aa4-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="15aa4-157">Utilizzare queste informazioni per determinare il nome del server in cui è presente il database degli account utente.</span><span class="sxs-lookup"><span data-stu-id="15aa4-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="15aa4-158">Se il server RAS è un server avanzato, ottenere il nome del server dell'account utente concatenando il prefisso " \\ \\ " con il nome restituito nel membro **wszLogonDomain** .</span><span class="sxs-lookup"><span data-stu-id="15aa4-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="15aa4-159">Questo è dovuto al fatto che per un server avanzato il nome di dominio di accesso locale corrisponde al nome del server.</span><span class="sxs-lookup"><span data-stu-id="15aa4-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="15aa4-160">Se il server RAS è una workstation, utilizzare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="15aa4-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15aa4-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15aa4-161">Requirements</span></span>



| <span data-ttu-id="15aa4-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="15aa4-162">Requirement</span></span> | <span data-ttu-id="15aa4-163">Valore</span><span class="sxs-lookup"><span data-stu-id="15aa4-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15aa4-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15aa4-164">Minimum supported client</span></span><br/> | <span data-ttu-id="15aa4-165">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15aa4-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="15aa4-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15aa4-166">Minimum supported server</span></span><br/> | <span data-ttu-id="15aa4-167">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="15aa4-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15aa4-168">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="15aa4-168">End of client support</span></span><br/>    | <span data-ttu-id="15aa4-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="15aa4-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="15aa4-170">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="15aa4-170">End of server support</span></span><br/>    | <span data-ttu-id="15aa4-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15aa4-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="15aa4-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15aa4-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="15aa4-173"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="15aa4-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15aa4-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15aa4-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15aa4-175">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="15aa4-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="15aa4-176">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="15aa4-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="15aa4-177">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="15aa4-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="15aa4-178">**\_statistiche porta \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="15aa4-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="15aa4-179">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="15aa4-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="15aa4-180">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="15aa4-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





