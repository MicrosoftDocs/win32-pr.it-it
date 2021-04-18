---
description: Usare le tecnologie di crittografia per la crittografia a chiave pubblica, gli algoritmi di crittografia, la crittografia RSA e i certificati digitali.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306447"
---
# <a name="cryptography"></a>Crittografia

## <a name="purpose"></a>Scopo

La crittografia prevede l'uso di codici per la conversione dei dati in modo che solo un destinatario specifico possa leggerlo, usando una chiave.

Le tecnologie di crittografia Microsoft includono CryptoAPI, provider del servizio di crittografia (CSP), strumenti CryptoAPI, capicol, WinTrust, emissione e gestione dei certificati e sviluppo di infrastrutture a chiave pubblica personalizzabili. Vengono descritti anche la registrazione di certificati e smart card, la gestione dei certificati e lo sviluppo di moduli personalizzati.

## <a name="developer-audience"></a>Sviluppatori

CryptoAPI è progettato per l'uso da parte di sviluppatori di applicazioni basate su Windows che consentono agli utenti di creare e scambiare documenti e altri dati in un ambiente protetto, soprattutto su supporti non protetti, ad esempio Internet. Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione Windows. Sebbene non sia obbligatorio, è consigliabile comprendere la crittografia o gli argomenti relativi alla sicurezza.

CAPICOM è un componente solo a 32 bit che deve essere utilizzato dagli sviluppatori che creano applicazioni utilizzando il linguaggio di programmazione di Visual Basic Scripting Edition (VBScript) o il linguaggio di programmazione C++. CAPICOM è disponibile per l'uso nei sistemi operativi specificati in Run-Time requirements. Per lo sviluppo futuro, è consigliabile usare la .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).

## <a name="run-time-requirements"></a>Requisiti di runtime

Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

CAPICOM 2.1.0.2 è supportato nei sistemi operativi e nelle versioni seguenti:

-   Windows Server 2003
-   Windows XP

CAPICOM è disponibile come file ridistribuibile che può essere scaricato da [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).

Servizi certificati richiede le seguenti versioni di questi sistemi operativi:

-   Windows Server 2008 R2
-   Windows Server 2008
-   Windows Server 2003

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                           | Descrizione                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulla crittografia](about-cryptography.md)<br/>         | Concetti chiave di crittografia e una panoramica di alto livello delle tecnologie di crittografia Microsoft.<br/>                                                                                                                           |
| [Uso della crittografia](using-cryptography.md)<br/>         | Processi di crittografia, procedure ed esempi estesi di programmi C e Visual Basic con funzioni CryptoAPI e oggetti CAPICOM.<br/>                                                                            |
| [Informazioni di riferimento sulla crittografia](cryptography-reference.md)<br/> | Descrizioni dettagliate delle funzioni di crittografia Microsoft, delle interfacce, degli oggetti, delle strutture e di altri elementi di programmazione. Include le descrizioni di riferimento dell'API per l'uso di certificati digitali.<br/> |



 

 

 




