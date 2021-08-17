---
title: Gerarchia del modello a oggetti
description: Gli oggetti nel modello a oggetti SDO sono disposti in una gerarchia. Ciò significa che gli oggetti in SDO forniscono l'accesso ad altri oggetti in SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f63b5692571bab49580251d6ef879adde8ae9a57af4c541404aabc48538e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063343"
---
# <a name="object-model-hierarchy"></a>Gerarchia del modello a oggetti

Gli oggetti nel modello a oggetti SDO sono disposti in una gerarchia. Ciò significa che gli oggetti in SDO forniscono l'accesso ad altri oggetti in SDO.

Gli oggetti forniscono l'accesso ad altri oggetti in due modi. Un modo è che l'oggetto esponga un'interfaccia che fornisce metodi per recuperare altri oggetti. Un esempio di questo approccio è l'oggetto Machine. L'oggetto Machine espone [**l'interfaccia ISdoMachine.**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) Il [**metodo ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera un oggetto Service. Il [**metodo ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera un oggetto utente.

![Oggetto computer che espone l'interfaccia isdomachine](images/sdo01.png)

Per altre informazioni, vedere [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).

Il secondo modo in cui gli oggetti forniscono l'accesso ad altri oggetti è rappresentato da una raccolta di oggetti come proprietà dell'oggetto che la contiene. Per recuperare una raccolta di oggetti, chiamare [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) sulla proprietà di un oggetto che rappresenta la raccolta. Ad esempio, per recuperare la raccolta Criteri, chiamare **ISdo::GetProperty sull'interfaccia** [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) esposta dall'oggetto NPS.

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete a partire da Windows Server 2008.

 

![recupero della raccolta di criteri](images/sdo02.png)

Per il codice di esempio che recupera la raccolta Criteri, vedere [Recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection).

[**L'oggetto dati del server dei**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) criteri di rete ha le proprietà seguenti che rappresentano le raccolte:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Conti
</dt> <dd>

L'unico revisore nella raccolta Auditors è [**il registro eventi NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Politiche
</dt> <dd>

Ogni [**oggetto criteri**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) ha una proprietà che rappresenta una raccolta di condizioni.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profili
</dt> <dd>

Ogni [**oggetto profilo**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) nelle raccolte Profiles ha una proprietà che rappresenta una raccolta di attributi. Per un elenco degli attributi supportati da [SDO,](/windows/desktop/Nps/sdo-sdo-supported-attributes) vedere Attributi supportati da SDO.

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolli
</dt> <dd>

La raccolta protocols contiene l'oggetto protocollo RADIUS, che contiene una raccolta di client che rappresenta i client RADIUS. Vedere [Aggiunta di un client per](/windows/desktop/Nps/sdo-adding-a-client) il codice di esempio che illustra come recuperare la raccolta client.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Criteri proxy
</dt> <dd>

Questa raccolta contiene i criteri di accesso alla rete usati per l'elaborazione della richiesta di connessione.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Profili proxy
</dt> <dd>

Questa raccolta contiene i profili usati per l'elaborazione della richiesta di connessione.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Gruppi di server RADIUS
</dt> <dd>

Ogni [**gruppo di server RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) nella raccolta gruppi di server RADIUS dispone di una proprietà che rappresenta la raccolta di server in tale gruppo di server.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Gestori richieste
</dt> <dd>

Questa raccolta contiene la raccolta "Microsoft Realms Evaluator". In questa raccolta sono disponibili anche le impostazioni "Microsoft NT SAM Authentication" e "Microsoft Accounting".

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti e proprietà SDO](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Attributi supportati da SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 