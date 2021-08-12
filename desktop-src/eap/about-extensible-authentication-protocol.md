---
title: Informazioni su EAP
description: Extensible Authentication Protocol (EAP), uno standard supportato da molti componenti di rete Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Extensible Authentication Protocol(Protocollo di autenticazione estendibile), descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84866f7f550213850bf95c39a6f0847df31bed3550db66139f2ec30bf921b5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276044"
---
# <a name="about-eap"></a>Informazioni su EAP

Questo argomento descrive Extensible Authentication Protocol (EAP), uno standard supportato da molti componenti di rete Microsoft.

## <a name="eap-components"></a>Componenti EAP

EAP è fondamentale per proteggere la sicurezza di RETI LAN wireless (802.1X), RETI LAN cablate e connessioni remote e reti private virtuali (VPN).

I componenti seguenti supportano il protocollo EAP.

-   I client e i server di Accesso remoto Microsoft per connessioni remote e VPN (PPTP e L2TP/IPSec) implementano EAP come estensione a PPP. Per altre informazioni, vedere [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   I client LAN wireless e cablati compatibili con Microsoft IEEE 802.1X implementano EAP come definito nella bozza standard IEEE 802.1X.
-   Il server RADIUS Microsoft, denominato IAS (Internet Authentication Service), implementa EAP come definito in [RFC 2865.](https://go.microsoft.com/fwlink/p/?linkid=84055)

Tutti i componenti precedenti supportano questa architettura estendibile tramite Microsoft Windows Software Development Kit (SDK), rendendo possibile l'integrazione di moduli di autenticazione di terze parti. Questo meccanismo estendibile può essere usato per supportare schede token, Kerberos, chiave pubblica e protocolli di autenticazione S/Key.

## <a name="protected-extensible-authentication-protocol"></a>Protocollo di autenticazione estendibile protetto

Oltre a EAP, l'implementazione wireless (802.1X) e il server RADIUS supportano anche uno standard emergente denominato PEAP (Protected EAP).

PEAP fornisce diversi servizi chiave ad altri protocolli di autenticazione EAP, come indicato di seguito.

-   PEAP crittografa i pacchetti EAP di altri protocolli di autenticazione EAP usando Transport Layer Security (TLS), una tecnologia basata su SSL (Secure Socket Layer). Per altre informazioni, vedere [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   PEAP autentica il lato server usando un certificato server, con il server RADIUS.
-   PEAP offre una funzionalità di ri-autenticazione rapida che supporta il roaming efficiente tra dispositivi wireless.
-   PEAP gestisce la frammentazione e il riasse assembly dei pacchetti EAP.
-   PEAP genera chiavi usate per crittografare il traffico wireless.

PEAP rende molto più semplice scrivere un protocollo EAP perché il programmatore non deve più risolvere questi problemi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su EAP ed EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




