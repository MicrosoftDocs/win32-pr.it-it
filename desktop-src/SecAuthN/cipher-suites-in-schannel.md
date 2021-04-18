---
description: Un pacchetto di crittografia è un set di algoritmi di crittografia.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Pacchetti di crittografia in TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa8b47aed266c49ac306adfd2aef78af269a39
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320978"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Pacchetti di crittografia in TLS/SSL (SSP Schannel)

Un pacchetto di crittografia è un set di algoritmi di crittografia. L'implementazione SSP Schannel dei protocolli TLS/SSL usa gli algoritmi di un pacchetto di crittografia per creare chiavi e crittografare le informazioni. Un pacchetto di crittografia specifica un algoritmo per ognuna delle attività seguenti:

-   Scambio di chiave
-   Crittografia di massa
-   Autenticazione dei messaggi

Gli [*algoritmi di scambio di chiave*](/windows/desktop/SecGloss/k-gly) proteggono le informazioni necessarie per creare chiavi condivise. Questi algoritmi sono asimmetrici ([*algoritmi a chiave pubblica*](/windows/desktop/SecGloss/p-gly)) ed eseguono prestazioni ottimali per quantità di dati relativamente ridotte.

Gli algoritmi di crittografia bulk crittografano i messaggi scambiati tra client e server. Questi algoritmi sono [*simmetrici*](/windows/desktop/SecGloss/s-gly) ed eseguono prestazioni ottimali per grandi quantità di dati.

Gli algoritmi di [autenticazione dei messaggi](message-authentication-codes-in-schannel.md) generano [*hash*](/windows/desktop/SecGloss/h-gly) e firme dei messaggi che assicurano l' [*integrità*](/windows/desktop/SecGloss/i-gly) di un messaggio.

Gli sviluppatori specificano questi elementi usando i tipi di dati di [**\_ ID ALG**](/windows/desktop/SecCrypto/alg-id) . Per altre informazioni, vedere [specifica delle crittografie Schannel e dei punti di forza di crittografia](specifying-schannel-ciphers-and-cipher-strengths.md).

Nelle versioni precedenti di Windows, i pacchetti di crittografia TLS e le curve ellittiche sono stati configurati usando una singola stringa:

![Diagramma che mostra una singola stringa per un pacchetto di crittografia.](images/tls-cipher-suite.png)

Diverse versioni di Windows supportano i diversi pacchetti di crittografia TLS e l'ordine di priorità. Vedere la versione di Windows corrispondente per l'ordine predefinito in cui vengono scelti dal provider Microsoft Schannel.

**Windows Server 2022:** Per informazioni sui pacchetti di crittografia supportati, vedere pacchetti [di crittografia TLS in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, versione 1903:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 V1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, versione 1809:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, versione 1803:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, versione 1709:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, versione 1703:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 e Windows 10, versione 1607:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10, versione 1511:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, versione 1507:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 10 V1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 e Windows 8.1:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa [ai pacchetti di crittografia TLS in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 e Windows 8:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 e Windows 7:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows 7](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 e Windows Vista:** Per informazioni sui pacchetti di crittografia supportati, vedere la pagina relativa ai pacchetti di [crittografia TLS in Windows Vista](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 e Windows XP:** Per informazioni sui pacchetti di crittografia supportati, vedere gli argomenti seguenti.

| Argomento                                                                         | Descrizione                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Pacchetti di crittografia TLS](tls-cipher-suites.md)<br/>                         | Informazioni sui pacchetti di crittografia disponibili con il protocollo TLS in Windows Server 2003 e Windows XP.<br/>              |
| [Protocollo Secure Sockets Layer](secure-sockets-layer-protocol.md)<br/> | Informazioni generali su SSL 2,0 e 3,0, inclusi i pacchetti di crittografia disponibili in Windows Server 2003 e Windows XP.<br/> |



 

> [!Note]  
> Prima di Windows 10, le stringhe del pacchetto di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica, quindi il suffisso della curva ellittica non è obbligatorio e viene sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di utilizzare criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.

 

