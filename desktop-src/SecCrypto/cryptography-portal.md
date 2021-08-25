---
description: Usare tecnologie di crittografia per la crittografia a chiave pubblica, gli algoritmi di crittografia, la crittografia RSA e i certificati digitali.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050f84d118cb5ad9e1da49ddabd73489745339bb0b1357e229b0f1609a1c997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876111"
---
# <a name="cryptography"></a>Crittografia

## <a name="purpose"></a>Scopo

La crittografia è l'uso di codici per convertire i dati in modo che solo un destinatario specifico possa leggerli usando una chiave.

Le tecnologie di crittografia Microsoft includono CryptoAPI, Cryptographic Service Provider (CSP), CryptoAPI Tools, CAPICOM, WinTrust, emissione e gestione dei certificati e sviluppo di infrastrutture a chiave pubblica personalizzabili. Vengono inoltre descritte la registrazione e smart card certificati, la gestione dei certificati e lo sviluppo di moduli personalizzati.

## <a name="developer-audience"></a>Sviluppatori

CryptoAPI è destinato all'uso da parte degli sviluppatori di applicazioni basate su Windows che consentiranno agli utenti di creare e scambiare documenti e altri dati in un ambiente sicuro, in particolare su supporti non sicuri come Internet. Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'Windows di programmazione. Sebbene non sia obbligatorio, è consigliabile comprendere gli argomenti relativi alla crittografia o alla sicurezza.

CAPICOM è un componente solo a 32 bit destinato agli sviluppatori che creano applicazioni usando il linguaggio di programmazione Visual Basic Scripting Edition (VBScript) o il linguaggio di programmazione C++. CAPICOM è disponibile per l'uso nei sistemi operativi specificati in Run-Time requisiti. Per lo sviluppo futuro, è consigliabile usare il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)

## <a name="run-time-requirements"></a>Requisiti di runtime

Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

CAPICOM 2.1.0.2 è supportato nei sistemi operativi e nelle versioni seguenti:

-   Windows Server 2003
-   Windows XP

CAPICOM è disponibile come file ridistribuibile che può essere scaricato da [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).

Servizi certificati richiede le versioni seguenti di questi sistemi operativi:

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                           | Descrizione                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulla crittografia](about-cryptography.md)<br/>         | Concetti relativi alla crittografia delle chiavi e una visualizzazione di alto livello delle tecnologie di crittografia Microsoft.<br/>                                                                                                                           |
| [Uso della crittografia](using-cryptography.md)<br/>         | Processi di crittografia, procedure ed esempi estesi di C e Visual Basic tramite funzioni CryptoAPI e oggetti CAPICOM.<br/>                                                                            |
| [Informazioni di riferimento sulla crittografia](cryptography-reference.md)<br/> | Descrizioni dettagliate di funzioni di crittografia Microsoft, interfacce, oggetti, strutture e altri elementi di programmazione. Include le descrizioni di riferimento dell'API per l'uso dei certificati digitali.<br/> |



 

 

 




