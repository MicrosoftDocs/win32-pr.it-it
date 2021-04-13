---
title: Informazioni su EAP
description: Extensible Authentication Protocol (EAP), uno standard supportato da molti componenti di rete Microsoft.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Protocollo di autenticazione estendibile, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399841"
---
# <a name="about-eap"></a>Informazioni su EAP

In questo argomento viene descritto il protocollo EAP (Extensible Authentication Protocol), uno standard supportato da molti componenti di rete Microsoft.

## <a name="eap-components"></a>Componenti EAP

Il protocollo EAP è essenziale per la protezione della sicurezza di reti LAN wireless (802.1 X), LAN cablate e connessioni remote e VPN (Virtual Private Network).

I componenti seguenti supportano il protocollo EAP.

-   I client e i server di accesso remoto Microsoft per la connessione remota e la VPN (PPTP e L2TP/IPSec) implementano EAP come estensione di PPP. Per ulteriori informazioni, vedere [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).
-   I client LAN wireless e cablati compatibili con Microsoft IEEE 802.1 X implementano EAP come definito nello standard Draft IEEE 802.1 X.
-   Server RADIUS Microsoft, denominato servizio di autenticazione Internet (IAS), implementa EAP come definito nella [specifica RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).

Tutti i componenti precedenti supportano questa architettura estendibile tramite il Software Development Kit (SDK) di Microsoft Windows, rendendo possibile l'integrazione dei moduli di autenticazione di terze parti. Questo meccanismo estensibile può essere utilizzato per supportare schede token, Kerberos, chiave pubblica e protocolli di autenticazione S/chiave.

## <a name="protected-extensible-authentication-protocol"></a>Protocollo di autenticazione estensibile protetto

Oltre a EAP, l'implementazione wireless (802.1 X) e il server RADIUS supportano anche uno standard emergente denominato PEAP (Protected EAP).

PEAP offre diversi servizi chiave per altri protocolli di autenticazione EAP, come indicato di seguito.

-   PEAP crittografa i pacchetti EAP di altri protocolli di autenticazione EAP utilizzando Transport Layer Security (TLS), una tecnologia basata su SSL (Secure Socket Layer). Per ulteriori informazioni, vedere [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).
-   PEAP autentica il lato server usando un certificato del server, con il server RADIUS.
-   PEAP offre funzionalità di riautenticazione rapida che supportano il roaming efficiente tra dispositivi wireless.
-   PEAP gestisce la frammentazione e il riassemblaggio dei pacchetti EAP.
-   PEAP genera le chiavi usate per crittografare il traffico wireless.

PEAP rende molto più semplice scrivere un protocollo EAP perché il programmatore non deve più risolvere questi problemi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su EAP e EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




