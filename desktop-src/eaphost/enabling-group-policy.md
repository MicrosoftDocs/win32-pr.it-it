---
title: Abilitazione Criteri di gruppo
description: Informazioni su come configurare il supplicant abilitando Criteri di gruppo. Vedere le considerazioni per i supplicant e visualizzare altre risorse disponibili.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2a388bf8dba155e42d5542c1379f7b0cc34d44579b92809387541d7e20cf65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785000"
---
# <a name="enabling-group-policy"></a>Abilitazione Criteri di gruppo

Questo argomento illustra come configurare il supplicant abilitando i criteri di gruppo. I supplicant EAPHost possono partecipare ai criteri di gruppo per consentire a un amministratore di rete di configurare centralmente i computer di rete.

Il metodo e il meccanismo precisi con cui il supplicant sceglie di partecipare ai criteri di gruppo è a discrezione del supplicant. Esempi di meccanismi per la partecipazione a Criteri di gruppo includono estensioni lato client/server, modello amministrativo e così via.

## <a name="considerations-when-enabling-group-policy"></a>Considerazioni sull'abilitazione Criteri di gruppo

Queste sono le considerazioni per i supplicant in relazione a Criteri di gruppo ed EAP.

1.  La configurazione EAP deve sempre essere archiviata come XML quando possibile e non in formato binario. I criteri di gruppo possono essere applicati a qualsiasi computer nel dominio e non è garantito che la configurazione del metodo EAP e i dati utente siano portabili tra le architetture del processore a 32 bit e a 64 bit. XML risolve i problemi di limite dell'architettura del processore poiché il supplicant converte localmente il codice XML indipendente dall'architettura del processore nella rappresentazione binaria della configurazione in fase di autenticazione.

    Per ulteriori informazioni, vedere gli argomenti seguenti.

    -   [Domande frequenti generali](general-frequently-asked-questions.md)
    -   [Domande frequenti sul metodo EAP](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Se viene usata un'estensione lato server di Criteri di gruppo, l'estensione chiamerà in genere [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) per determinare i metodi disponibili e generare la configurazione EAP appropriata per tali criteri. I criteri vengono quindi inviati ai client di rete appropriati in cui viene applicato il criterio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione del metodo EAP Interfaccia utente](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementazione del In-Band di Protezione accesso alla rete per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementazione del supporto di Protezione accesso alla rete per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Trasferimento di dati tra i metodi Supplicant ed EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




