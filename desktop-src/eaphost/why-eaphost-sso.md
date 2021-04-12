---
title: Panoramica dello scenario EAPHost SSO
description: Contiene due scenari che illustrano i vantaggi di un supplicant abilitato per l'accesso Single Sign-on (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104117241"
---
# <a name="sso-eaphost-scenario-overview"></a>Panoramica dello scenario EAPHost SSO

Nell'argomento seguente sono inclusi due scenari in cui vengono illustrati i vantaggi di un supplicant abilitato per l'accesso Single Sign-on (SSO).

## <a name="about-the-scenarios"></a>Informazioni sugli scenari

SSO fornisce funzionalità per conservare informazioni aggiuntive sulle credenziali utente rispetto a quelle tradizionalmente archiviate nel BLOB utente EAP. A differenza di altri processi di credenziali, i supplicant abilitati per SSO possono risolvere situazioni di accesso come il roaming di AP e la modifica della password senza l'intervento dell'utente.

## <a name="sso-eap-tls-pin-caching-behavior"></a>Comportamento della memorizzazione nella cache del PIN SSO EAP-TLS

Un supplicant può tentare di eseguire l'autenticazione di rete usando un metodo EAP basato su smart card, ad esempio Extensible Authentication Protocol Transport Layer Security (EAP-TLS). In questo e in scenari simili, il supplicant ottiene il PIN della smart card dall'utente e recupera un certificato utente per l'autenticazione di rete seguito da una chiamata a WinLogin nel computer locale. Al termine dell'autenticazione, il richiedente memorizza nella cache il BLOB utente e non archivia le informazioni sul PIN dell'utente.

Quando l'utente si sposta in un percorso di ripresa della sessione diverso ed è necessario ripetere l'autenticazione. Poiché non è possibile archiviare il certificato con pre-accesso, l'autenticazione utente avrà esito negativo e il richiedente Scarica il BLOB utente. A questo punto, il PIN dell'utente è necessario per recuperare il certificato utente dalla smart card per l'autenticazione di rete. Poiché SSO memorizza nella cache il PIN, il certificato può essere recuperato senza l'intervento dell'utente. Senza SSO, EAP-TLS dovrebbe generare nuovamente un'interfaccia utente per la raccolta di PIN.

Per un approccio dettagliato, vedere comportamento di caching del [pin SSO EAP-TLS](sso-eap-tls-pin-caching-behavior-.md).

## <a name="sso-password-change-behavior"></a>Comportamento di modifica della password SSO

Un supplicant può tentare di eseguire l'autenticazione di rete usando un metodo EAP basato su password, ad esempio Microsoft Challenge Handshake Authentication Protocol versione 2,0 (MS-CHAPv2), configurato per usare le credenziali di WinLogin. In questo scenario, il supplicant raccoglie le credenziali utente una volta e le fornisce a EAPHost per l'autenticazione di rete. Al termine dell'autenticazione di rete, il supplicant usa lo stesso set di credenziali per WinLogin.

Tuttavia, se le credenziali, ad esempio la password dell'utente sono state modificate durante l'autenticazione di rete senza un supplicant abilitato per SSO, la successiva chiamata a WinLogin provocherà un errore. SSO mantiene le nuove credenziali e consente un WinLogin riuscito senza ulteriori interventi da parte dell'utente.

Per un approccio dettagliato, vedere comportamento di modifica della [password SSO](sso-password-change-behavior-.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SSO e PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




