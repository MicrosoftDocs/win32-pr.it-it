---
title: Autenticazione, autorizzazione e accounting RADIUS
description: NPS supporta completamente il protocollo Remote Authentication Dial-In User Service (RADIUS). Il protocollo RADIUS è lo standard de facto per l'autenticazione utente remota ed è documentato in RFC 2865 e RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399401"
---
# <a name="radius-authentication-authorization-and-accounting"></a>Autenticazione, autorizzazione e accounting RADIUS

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

NPS supporta completamente il protocollo Remote Authentication Dial-In User Service (RADIUS). Il protocollo RADIUS è lo standard de facto per l'autenticazione utente remota ed è documentato in [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-authentication-and-authorization"></a>Autenticazione e autorizzazione RADIUS

Il diagramma seguente mostra un client di autenticazione ("utente") che si connette a un server di accesso alla rete (NAS) tramite una connessione remota, usando il Point-to-Point Protocol (PPP). Per autenticare l'utente, il NAS Contatta un server remoto che esegue NPS. Il NAS e il server NPS comunicano tramite il protocollo RADIUS.

![autenticazione utente remoto](images/ias01.png)

Un NAS funziona come un client di un server o di server che supportano il protocollo RADIUS. I server che supportano il protocollo RADIUS vengono in genere definiti server RADIUS. Il client RADIUS, ovvero il NAS, passa le informazioni relative all'utente ai server RADIUS designati, quindi agisce sulla risposta restituita dai server. La richiesta inviata dal NAS al server RADIUS per autenticare l'utente è in genere denominata "richiesta di autenticazione".

Se un server RADIUS autentica l'utente correttamente, il server RADIUS restituisce al NAS le informazioni di configurazione in modo da poter fornire al servizio di rete l'utente. Queste informazioni di configurazione sono costituite da "autorizzazioni" e contengono, tra le altre, il tipo di servizio che può fornire all'utente (ad esempio, PPP o Telnet).

Mentre il server RADIUS sta elaborando la richiesta di autenticazione, può eseguire funzioni di autorizzazione, ad esempio verificare il numero di telefono dell'utente e verificare se l'utente ha già una sessione in corso. Il server RADIUS può determinare se l'utente dispone già di una sessione in corso contattando un server di stato.

Per ulteriori informazioni sull'autenticazione e l'autorizzazione RADIUS, vedere [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>Accounting RADIUS

Il server RADIUS raccoglie anche un'ampia gamma di informazioni inviate dal NAS che possono essere usate per l'accounting e per la creazione di report sull'attività di rete. Il client RADIUS invia le informazioni ai server RADIUS designati quando l'utente si connette e si disconnette. Il client RADIUS può inviare informazioni aggiuntive sull'utilizzo a intervalli regolari mentre è in corso la sessione. Le richieste inviate dal client al server per registrare le informazioni di accesso/disconnessione e di utilizzo vengono in genere denominate "richieste di contabilità".

Per ulteriori informazioni sull'accounting RADIUS, vedere [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>Proxy RADIUS

Un server RADIUS può fungere da client proxy per altri server RADIUS. In questi casi, il server RADIUS contattato dal NAS passa la richiesta di autenticazione o di accounting a un altro server RADIUS che esegue effettivamente l'autenticazione o l'attività di contabilità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Pacchetti accounting RADIUS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Utilizzo di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 