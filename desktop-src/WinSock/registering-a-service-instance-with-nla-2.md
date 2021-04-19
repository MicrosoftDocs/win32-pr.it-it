---
description: I client NLA possono registrare le informazioni di configurazione di rete a livello di sistema, consentendo alle query future di restituire le informazioni di configurazione specificate indipendentemente dal fatto che la rete sia attiva.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrazione di un'istanza del servizio con NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310454"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="246e2-103">Registrazione di un'istanza del servizio con NLA</span><span class="sxs-lookup"><span data-stu-id="246e2-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="246e2-104">I client NLA possono registrare le informazioni di configurazione di rete a livello di sistema, consentendo alle query future di restituire le informazioni di configurazione specificate indipendentemente dal fatto che la rete sia attiva.</span><span class="sxs-lookup"><span data-stu-id="246e2-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="246e2-105">Questa funzionalità consente ai client NLA di influenzare un'esperienza utente di informazioni di rete coerente in più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="246e2-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="246e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="246e2-106">Parameters</span></span>

<span data-ttu-id="246e2-107">Per registrare un'istanza del servizio con il provider del servizio di riconoscimento del percorso di rete, usare la funzione [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) .</span><span class="sxs-lookup"><span data-stu-id="246e2-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="246e2-108">Per registrare correttamente un'istanza del servizio, è necessario impostare determinati parametri della funzione **WSASetService** con le informazioni appropriate, come illustrato in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="246e2-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="246e2-109">Per riferimento rapido, la funzione **WSASetService** presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="246e2-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="246e2-110">Per il parametro *lpqsRegInfo* , fornire una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) da un risultato della query NLA SP o costruita rispettando i requisiti di una query NLA SP, come specificato in [query NLA](querying-nla-2.md).</span><span class="sxs-lookup"><span data-stu-id="246e2-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="246e2-111">Di seguito sono riportate le operazioni supportate per il parametro *essOperation* :</span><span class="sxs-lookup"><span data-stu-id="246e2-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="246e2-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>\_Registro RNRSERVICE</span><span class="sxs-lookup"><span data-stu-id="246e2-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="246e2-113">La rete definita nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornita in *lpqsRegInfo* viene resa persistente per l'utente attivo archiviando l'istanza di rete nell'hive del registro di sistema per l'utente corrente, che consente la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="246e2-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="246e2-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>eliminazione di RNRSERVICE \_</span><span class="sxs-lookup"><span data-stu-id="246e2-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="246e2-115">Se la rete definita nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornita in *lpqsRegInfo* è persistente, verrà rimossa.</span><span class="sxs-lookup"><span data-stu-id="246e2-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="246e2-116">L'operazione specificata nel parametro *essOperation* può essere modificata dalle opzioni seguenti, che è possibile specificare con la logica o binario:</span><span class="sxs-lookup"><span data-stu-id="246e2-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="246e2-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nome descrittivo NLA \_</span><span class="sxs-lookup"><span data-stu-id="246e2-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="246e2-118">Quando viene usato con \_ il registro RNRSERVICE, viene verificata la validità del campo *lpszComment* della rete definito in *lpqsRegInfo* , che viene archiviato in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="246e2-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="246e2-119">Se usato con RNRSERVICE \_ Delete e la rete definita ha un nome descrittivo, il nome descrittivo viene rimosso, ma la voce di rete rimane intatta.</span><span class="sxs-lookup"><span data-stu-id="246e2-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="246e2-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_rete ALLUSERS \_ NLA</span><span class="sxs-lookup"><span data-stu-id="246e2-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="246e2-121">Quando viene usato con \_ il registro RNRSERVICE, la voce viene archiviata in modo permanente in HKEY \_ \_ computer locale, rendendola disponibile durante le query a tutti gli utenti nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="246e2-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="246e2-122">Se usato con RNRSERVICE \_ Delete, la rete specificata viene rimossa dal \_ computer locale HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="246e2-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="246e2-123">Se la rete specificata non è presente, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="246e2-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="246e2-124">Per eliminare una rete dall'hive del registro di sistema dell'utente corrente, questo flag non deve essere specificato.</span><span class="sxs-lookup"><span data-stu-id="246e2-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="246e2-125">Questo flag è valido solo nel contesto di sicurezza di un amministratore di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="246e2-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="246e2-126">NLA supporta i codici di errore seguenti per le chiamate di funzione [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="246e2-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="246e2-127">Errore</span><span class="sxs-lookup"><span data-stu-id="246e2-127">Error</span></span>             | <span data-ttu-id="246e2-128">Significato</span><span class="sxs-lookup"><span data-stu-id="246e2-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="246e2-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="246e2-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="246e2-130">Una chiamata riuscita alla funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare NLA non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="246e2-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="246e2-131">WSAEACCESS</span><span class="sxs-lookup"><span data-stu-id="246e2-131">WSAEACCESS</span></span>        | <span data-ttu-id="246e2-132">\_ \_ La rete ALLUSERS NLA è stata specificata in *dwControlFlags* mentre non è presente nel contesto di sicurezza di un amministratore di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="246e2-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="246e2-133">WSAEALREADY</span><span class="sxs-lookup"><span data-stu-id="246e2-133">WSAEALREADY</span></span>       | <span data-ttu-id="246e2-134">La rete specificata è già archiviata in modo permanente nella modalità richiesta e non è stato specificato alcun flag in *dwControlFlags* per indicare un aggiornamento alla voce esistente.</span><span class="sxs-lookup"><span data-stu-id="246e2-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="246e2-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="246e2-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="246e2-136">È stata specificata una famiglia di protocolli per la quale non è disponibile alcun supporto.</span><span class="sxs-lookup"><span data-stu-id="246e2-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="246e2-137">In NLA sono supportate solo le famiglie di protocolli IP.</span><span class="sxs-lookup"><span data-stu-id="246e2-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="246e2-138">WSAEPFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="246e2-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="246e2-139">È stato specificato un protocollo per il quale non è disponibile alcun supporto.</span><span class="sxs-lookup"><span data-stu-id="246e2-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="246e2-140">In NLA è supportato solo il protocollo IP.</span><span class="sxs-lookup"><span data-stu-id="246e2-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



