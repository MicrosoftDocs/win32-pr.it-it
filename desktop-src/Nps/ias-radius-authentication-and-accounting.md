---
title: Autenticazione, autorizzazione e accounting RADIUS
description: Server dei criteri di rete supporta completamente il Remote Authentication Dial-In User Service (RADIUS). Il protocollo RADIUS è lo standard di fatto per l'autenticazione utente remota ed è documentato in RFC 2865 e RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b0395b6bc147da4f78bb718cda714014b9b665f5a26a8d20fa29402ee8dec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063497"
---
# <a name="radius-authentication-authorization-and-accounting"></a>Autenticazione, autorizzazione e accounting RADIUS

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.

 

Server dei criteri di rete supporta completamente il Remote Authentication Dial-In User Service (RADIUS). Il protocollo RADIUS è lo standard di fatto per l'autenticazione utente remota ed è documentato in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866.](https://www.ietf.org/rfc/rfc2866.txt)

## <a name="radius-authentication-and-authorization"></a>Autenticazione e autorizzazione RADIUS

Il diagramma seguente illustra un client di autenticazione ("Utente") che si connette a un server di accesso alla rete (NAS) tramite una connessione remota, usando Point-to-Point Protocol (PPP). Per autenticare l'utente, il NAS contatta un server remoto che esegue Server dei criteri di rete. Il server NAS e il server NPS comunicano usando il protocollo RADIUS.

![autenticazione utente remoto](images/ias01.png)

Un NAS opera come client di uno o più server che supportano il protocollo RADIUS. I server che supportano il protocollo RADIUS vengono in genere definiti server RADIUS. Il client RADIUS, ci esempio il NAS, passa le informazioni sull'utente ai server RADIUS designati e quindi agisce sulla risposta restituita dal server. La richiesta inviata dal NAS al server RADIUS per autenticare l'utente viene in genere definita "richiesta di autenticazione".

Se un server RADIUS autentica correttamente l'utente, il server RADIUS restituisce informazioni di configurazione al NAS in modo che possa fornire il servizio di rete all'utente. Queste informazioni di configurazione sono costituite da "autorizzazioni" e contengono, tra le altre, il tipo di servizio NAS che può fornire all'utente (ad esempio, PPP o telnet).

Mentre il server RADIUS sta elaborando la richiesta di autenticazione, può eseguire funzioni di autorizzazione, ad esempio verificare il numero di telefono dell'utente e verificare se l'utente ha già una sessione in corso. Il server RADIUS può determinare se l'utente ha già una sessione in corso contattando un server di stato.

Per altre informazioni sull'autenticazione e sull'autorizzazione RADIUS, vedere [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>RADIUS Accounting

Il server RADIUS raccoglie anche un'ampia gamma di informazioni inviate dal NAS che possono essere usate per l'accounting e per la creazione di report sulle attività di rete. Il client RADIUS invia informazioni ai server RADIUS designati quando l'utente accede e si disconnette. Il client RADIUS può inviare informazioni aggiuntive sull'utilizzo su base periodica mentre la sessione è in corso. Le richieste inviate dal client al server per registrare le informazioni di accesso/disconnessione e utilizzo sono in genere chiamate "richieste di accounting".

Per altre informazioni sull'accounting RADIUS, vedere [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>Proxy RADIUS

Un server RADIUS può fungere da client proxy per altri server RADIUS. In questi casi, il server RADIUS contattato dal NAS passa la richiesta di autenticazione o accounting a un altro server RADIUS che esegue effettivamente l'autenticazione o l'attività di accounting.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Pacchetti di accounting RADIUS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Uso di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 