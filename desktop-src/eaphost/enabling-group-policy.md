---
title: Abilitazione di Criteri di gruppo
description: Informazioni su come configurare il supplicant abilitando criteri di gruppo. Vedere Considerazioni per i supplicant e visualizzare altre risorse disponibili.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399743"
---
# <a name="enabling-group-policy"></a>Abilitazione di Criteri di gruppo

In questo argomento viene illustrato come configurare il supplicant abilitando criteri di gruppo. I supplicant EAPHost possono partecipare a criteri di gruppo per consentire a un amministratore di rete di configurare centralmente i computer di rete.

Il metodo e il meccanismo preciso con cui il supplicant sceglie di partecipare a criteri di gruppo è a discrezione del supplicante. Esempi di meccanismi per la partecipazione a criteri di gruppo includono estensioni lato client/server, modelli amministrativi e così via.

## <a name="considerations-when-enabling-group-policy"></a>Considerazioni per l'abilitazione di Criteri di gruppo

Queste sono le considerazioni per i supplicant rispetto a criteri di gruppo e EAP.

1.  La configurazione EAP deve sempre essere archiviata come XML quando possibile e non nel formato binario. Criteri di gruppo può essere applicato a qualsiasi computer nel dominio e la configurazione del metodo EAP e i dati utente non sono necessariamente portabili tra architetture di processori a 32 bit e 64 bit. Il codice XML risolve i problemi di limite dell'architettura del processore perché il supplicant converte localmente l'XML indipendente dall'architettura del processore alla rappresentazione binaria della configurazione al momento dell'autenticazione.

    Per ulteriori informazioni, vedere gli argomenti seguenti.

    -   [Domande frequenti generali](general-frequently-asked-questions.md)
    -   [Domande frequenti sul metodo EAP](eap-method-frequently-asked-questions.md).
    -   [**EapHostPeerConfigXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [**EapHostPeerCredentialsXml2Blob**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  Se viene utilizzata un'estensione lato server di criteri di gruppo, l'estensione chiamerà in genere [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) per determinare i metodi disponibili e per generare la configurazione EAP appropriata per quel criterio. Il criterio viene quindi inviato ai client di rete appropriati in cui viene applicato il criterio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'interfaccia utente del metodo EAP](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Implementazione del supporto di In-Band NAP per i metodi EAP](enabling-in-band-nap-support.md)
</dt> <dt>

[Implementazione del supporto NAP per i metodi EAP](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Trasferimento di dati tra i metodi supplicant e EAP](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[Supplicant EAPHost](eaphost-supplicants.md)
</dt> </dl>

 

 




