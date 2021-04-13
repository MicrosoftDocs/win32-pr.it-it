---
title: Gerarchia del modello a oggetti
description: Gli oggetti nel modello a oggetti SDO sono disposti in una gerarchia. Questo significa che gli oggetti in SDO forniscono l'accesso ad altri oggetti in SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399305"
---
# <a name="object-model-hierarchy"></a>Gerarchia del modello a oggetti

Gli oggetti nel modello a oggetti SDO sono disposti in una gerarchia. Questo significa che gli oggetti in SDO forniscono l'accesso ad altri oggetti in SDO.

Gli oggetti consentono di accedere ad altri oggetti in due modi. Un modo consiste nell'esporre un'interfaccia che fornisce metodi per il recupero di altri oggetti da parte dell'oggetto. Un esempio di questo approccio è l'oggetto computer. L'oggetto computer espone l'interfaccia [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) . Il metodo [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera un oggetto servizio. Il metodo [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera un oggetto utente.

![oggetto computer che espone l'interfaccia isdomachine](images/sdo01.png)

Per ulteriori informazioni, vedere [ottenere il servizio e l'utente SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).

Il secondo modo in cui gli oggetti forniscono l'accesso ad altri oggetti è che una raccolta di oggetti viene rappresentata come una proprietà dell'oggetto che lo contiene. Per recuperare una raccolta di oggetti, chiamare [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) sulla proprietà di un oggetto che rappresenta la raccolta. Ad esempio, per recuperare la raccolta di criteri, chiamare **ISdo:: GetProperty** sull'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) esposta dall'oggetto NPS.

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.

 

![recupero della raccolta di criteri](images/sdo02.png)

Per il codice di esempio che recupera la raccolta di criteri, vedere [recupero di una raccolta](/windows/desktop/Nps/sdo-retrieving-a-collection).

L' [**oggetto dati del server NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) presenta le proprietà seguenti che rappresentano le raccolte:

<dl> <dt>

<span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Revisori
</dt> <dd>

L'unico revisore della raccolta revisori è il [**registro eventi NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).

</dd> <dt>

<span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Criteri
</dt> <dd>

Ogni [**oggetto Policy**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) dispone di una proprietà che rappresenta una raccolta di condizioni.

</dd> <dt>

<span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profili
</dt> <dd>

Ogni [**oggetto profilo**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) nelle raccolte di profili dispone di una proprietà che rappresenta una raccolta di attributi. Per un elenco degli attributi supportati da SDO, vedere [attributi supportati da SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) .

</dd> <dt>

<span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolli
</dt> <dd>

La raccolta Protocols contiene l'oggetto protocollo RADIUS, che contiene una raccolta clients che rappresenta i client RADIUS. Vedere [aggiunta di un client](/windows/desktop/Nps/sdo-adding-a-client) per il codice di esempio che illustra come recuperare la raccolta client.

</dd> <dt>

<span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Criteri proxy
</dt> <dd>

Questa raccolta contiene i criteri di accesso alla rete utilizzati per l'elaborazione delle richieste di connessione.

</dd> <dt>

<span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Profili proxy
</dt> <dd>

Questa raccolta contiene i profili utilizzati per l'elaborazione della richiesta di connessione.

</dd> <dt>

<span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Gruppi di server RADIUS
</dt> <dd>

Ogni [**gruppo di server RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) nella raccolta di gruppi di server RADIUS dispone di una proprietà che rappresenta la raccolta di server in tale gruppo di server.

</dd> <dt>

<span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Gestori di richieste
</dt> <dd>

Questa raccolta contiene la raccolta "Microsoft Realms Evaluator". In questa raccolta sono disponibili anche le impostazioni "autenticazione SAM Microsoft NT" e "Accounting Microsoft".

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti e proprietà di SDO](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[Attributi supportati da SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 