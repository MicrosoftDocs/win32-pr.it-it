---
title: Panoramica dello scenario SSO EAPHost
description: Contiene due scenari che illustrano i vantaggi di un supplicant abilitato per Single Sign-On (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc9be7af26844004073f21154df5ac12cb44d4eaa04fddc457b729ffe5e1083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042779"
---
# <a name="sso-eaphost-scenario-overview"></a>Panoramica dello scenario SSO EAPHost

L'argomento seguente contiene due scenari che illustrano i vantaggi di un supplicant abilitato per Single Sign-On (SSO).

## <a name="about-the-scenarios"></a>Informazioni sugli scenari

L'accesso Single Sign-On offre funzionalità per mantenere informazioni aggiuntive sulle credenziali utente rispetto a quelle tradizionalmente archiviate nel BLOB utente EAP. A differenza di altri processi di credenziali, i supplicant abilitati per l'accesso Single Sign-On possono risolvere situazioni di accesso come il roaming ap e la modifica della password senza l'intervento dell'utente.

## <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamento Caching pin SSO EAP-TLS

Un supplicant può tentare l'autenticazione di rete usando un metodo EAP basato su smart card, ad esempio Extensible Authentication Protocol Transport Layer Security (EAP-TLS). In questo e in scenari simili, il supplicante ottiene il PIN della smart card dall'utente e recupera un certificato utente per l'autenticazione di rete seguito da una chiamata a WinLogin nel computer locale. Al termine dell'autenticazione, il supplicant memorizza nella cache il BLOB dell'utente e non archivia le informazioni sul PIN dell'utente.

Quando l'utente esegue il roaming in un percorso diverso, deve essere eseguita la ripresa e la nuova autenticazione. Poiché il certificato non può essere archiviato prima dell'accesso, l'autenticazione utente avrà esito negativo e il supplicant scarica il BLOB dell'utente. A questo punto è necessario il PIN dell'utente per recuperare il certificato utente dalla smart card per l'autenticazione di rete. Poiché l'accesso SSO memorizza nella cache il PIN, il certificato può essere recuperato senza l'intervento dell'utente. Senza l'accesso Single Sign-On, EAP-TLS dovrebbe generare nuovamente un'interfaccia utente della raccolta di PIN.

Per un approccio dettagliata, vedere [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).

## <a name="sso-password-change-behavior"></a>Comportamento di modifica della password SSO

Un supplicant può tentare l'autenticazione di rete usando un metodo EAP basato su password, ad esempio Microsoft Challenge Handshake Authentication Protocol versione 2.0 (MS-CHAPv2), configurato per l'uso delle credenziali WinLogin. In questo scenario, il supplicante raccoglie le credenziali utente una sola volta e le fornisce a EAPHost per l'autenticazione di rete. Al termine dell'autenticazione di rete, il supplicant usa lo stesso set di credenziali per WinLogin.

Tuttavia, se durante l'autenticazione di rete sono state modificate credenziali come la password utente senza un supplicant abilitato per l'accesso SSO, la chiamata WinLogin successiva genererà un errore. L'accesso Single Sign-On mantiene le nuove credenziali e consente l'esito positivo di WinLogin senza l'intervento dell'utente aggiuntivo.

Per un approccio passo passo, vedere Comportamento di modifica [della password SSO.](sso-password-change-behavior-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




