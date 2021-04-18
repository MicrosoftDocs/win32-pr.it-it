---
title: Protocollo Kerberos V5
description: Protocollo Kerberos V5
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299473"
---
# <a name="kerberos-v5-protocol"></a>Protocollo Kerberos V5

Il protocollo di autenticazione Kerberos V5 dispone di un identificatore del servizio di autenticazione di RPC \_ C \_ AuthN \_ GSS \_ Kerberos. Il protocollo Kerberos definisce il modo in cui i client interagiscono con un servizio di autenticazione di rete ed è stato standardizzato da Internet Engineering Task Force (IETF) nel settembre 1993, nel documento [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt). I client ottengono ticket dal centro di distribuzione chiave Kerberos (KDC, Kerberos Key Distribution Center) e quindi presentano questi ticket ai server durante la procedura di connessione. I ticket Kerberos rappresentano le credenziali di rete del client.

Come NTLM, il protocollo Kerberos usa il nome di dominio, il nome utente e la password per rappresentare l'identità del client. Il ticket Kerberos iniziale ottenuto dal KDC quando l'utente esegue l'accesso si basa su un hash crittografato della password dell'utente. Questo ticket iniziale viene memorizzato nella cache. Quando l'utente tenta di connettersi a un server, il protocollo Kerberos controlla la cache dei ticket per un ticket valido per il server. Se non ne è disponibile uno, il Ticket iniziale per l'utente viene inviato al KDC insieme a una richiesta di un ticket per il server specificato. Il ticket di sessione viene aggiunto alla cache e può essere usato per connettersi allo stesso server fino alla scadenza del ticket.

Quando un server chiama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) usando il protocollo Kerberos, vengono restituiti il nome di dominio e il nome utente del client. Quando un server chiama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), viene restituito il token del client. Questi comportamenti sono gli stessi di quando si usa NTLM.

Il protocollo Kerberos funziona oltre i limiti del computer. I computer client e server devono essere entrambi in domini e tali domini devono avere una relazione di trust.

Il protocollo Kerberos richiede l'autenticazione reciproca e la supporta in modalità remota. Il client deve specificare il nome dell'entità del server e l'identità del server deve corrispondere esattamente al nome dell'entità. Se il client specifica **null** per il nome dell'entità del server o se il nome dell'entità non corrisponde al server, la chiamata avrà esito negativo.

Con il protocollo Kerberos, è possibile utilizzare i livelli di rappresentazione per identificare, rappresentare e delegare. Quando un server chiama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), il token restituito è valido dal computer per un periodo di tempo compreso tra 5 minuti e 8 ore. Al termine di questo periodo di tempo, può essere utilizzato solo sul computer server. Se un server è "Run As Activator" e l'attivazione viene eseguita con il protocollo Kerberos, il token del server scadrà tra 5 minuti e 8 ore dopo l'attivazione.

Il protocollo di autenticazione Kerberos V5 implementato da Windows supporta il [mascheramento](cloaking.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti COM e di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 




