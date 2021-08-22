---
description: Un pacchetto di crittografia è un set di algoritmi di crittografia.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Pacchetti di crittografia in TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590012b4a1ef0c84b8216fd970d1e60c8ed449294ec110dc566e7c3679b7bb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141220"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Pacchetti di crittografia in TLS/SSL (SSP Schannel)

Un pacchetto di crittografia è un set di algoritmi di crittografia. L'implementazione SSP schannel dei protocolli TLS/SSL usa algoritmi di un pacchetto di crittografia per creare chiavi e crittografare le informazioni. Un pacchetto di crittografia specifica un algoritmo per ognuna delle attività seguenti:

-   Scambio di chiave
-   Crittografia di massa
-   Autenticazione dei messaggi

[*Gli algoritmi di scambio delle chiavi*](/windows/desktop/SecGloss/k-gly) proteggono le informazioni necessarie per creare chiavi condivise. Questi algoritmi sono asimmetrici (algoritmi [*a chiave pubblica)*](/windows/desktop/SecGloss/p-gly)e sono molto validi per quantità relativamente ridotte di dati.

Gli algoritmi di crittografia bulk crittografano i messaggi s scambiati tra client e server. Questi algoritmi sono [*simmetrici e*](/windows/desktop/SecGloss/s-gly) sono molto validi per grandi quantità di dati.

[Gli algoritmi di](message-authentication-codes-in-schannel.md) autenticazione dei messaggi generano [*hash e*](/windows/desktop/SecGloss/h-gly) firme dei messaggi che garantiscono [*l'integrità*](/windows/desktop/SecGloss/i-gly) di un messaggio.

Gli sviluppatori specificano questi elementi usando i [**tipi di dati \_ ID ALG.**](/windows/desktop/SecCrypto/alg-id) Per altre informazioni, vedere [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).

Nelle versioni precedenti di Windows, i pacchetti di crittografia TLS e le curve ellittiche venivano configurati usando una singola stringa:

![Diagramma che mostra una singola stringa per un pacchetto di crittografia.](images/tls-cipher-suite.png)

Versioni Windows supportano diversi pacchetti di crittografia TLS e l'ordine di priorità. Vedere la versione Windows per l'ordine predefinito in cui vengono scelti dal provider Microsoft Schannel.

**Windows Server 2022:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows Server 2022](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, versione 1903:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, versione 1809:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, versione 1803:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10 versione 1709:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10 versione 1703:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 e Windows 10 versione 1607:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10 versione 1511:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10 versione 1507:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 e Windows 8.1:** Per informazioni sui pacchetti di crittografia supportati, vedere [Pacchetti di crittografia TLS in Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 e Windows 8:** Per informazioni sui pacchetti di crittografia supportati, vedere [Pacchetti di crittografia TLS in Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 e Windows 7:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows 7](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 e Windows Vista:** Per informazioni sui pacchetti di crittografia supportati, vedere Pacchetti di crittografia [TLS in Windows Vista](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 e Windows XP:** Per informazioni sui pacchetti di crittografia supportati, vedere gli argomenti seguenti.

| Argomento                                                                         | Descrizione                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Pacchetti di crittografia TLS](tls-cipher-suites.md)<br/>                         | Informazioni sui pacchetti di crittografia disponibili con il protocollo TLS in Windows Server 2003 e Windows XP.<br/>              |
| [protocollo Secure Sockets Layer](secure-sockets-layer-protocol.md)<br/> | Informazioni generali su SSL 2.0 e 3.0, inclusi i pacchetti di crittografia disponibili in Windows Server 2003 e Windows XP.<br/> |



 

> [!Note]  
> Prima di Windows 10, le stringhe del gruppo di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica in modo che il suffisso a curva ellittica non sia obbligatorio e venga sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di usare Criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.

 

