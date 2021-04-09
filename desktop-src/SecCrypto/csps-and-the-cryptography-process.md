---
description: Le funzioni CryptoAPI utilizzano i provider del servizio di crittografia (CSP) per eseguire la crittografia e la decrittografia e fornire l'archiviazione e la sicurezza chiave.
ms.assetid: 7977e59b-7ce1-4bb4-aae4-d67b7d646493
title: CSP e il processo di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5404fc3641a9a2c753158f5acb84850f3f0f29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049424"
---
# <a name="csps-and-the-cryptography-process"></a>CSP e il processo di crittografia

Le funzioni [*CryptoAPI*](../secgloss/c-gly.md) utilizzano i [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per eseguire la crittografia e la decrittografia e fornire l'archiviazione e la sicurezza chiave. Questi CSP sono moduli indipendenti. Idealmente, i CSP vengono scritti in modo da essere indipendenti da una particolare applicazione, in modo che qualsiasi applicazione venga eseguita con diversi CSP. In realtà, tuttavia, alcune applicazioni hanno requisiti specifici che richiedono un CSP personalizzato. Viene confrontato con il modello [*GDI*](../secgloss/g-gly.md) di Windows. I CSP sono analoghi ai driver di dispositivo grafici.

La qualità della protezione delle chiavi all'interno del sistema è un parametro di progettazione del CSP e non del sistema nel suo complesso. Questo consente l'esecuzione di un'applicazione in diversi contesti di sicurezza senza modifiche.

Per le applicazioni di accesso è necessario limitare con attenzione gli elementi interni crittografici. Ciò facilita lo sviluppo di applicazioni sicure e portatili.

Si applicano le tre regole di progettazione seguenti:

-   Le applicazioni non possono accedere direttamente al materiale delle chiavi. Poiché tutti i materiali delle chiavi vengono generati all'interno del CSP e utilizzati dall'applicazione tramite handle opachi, non vi è alcun rischio che un'applicazione o le DLL associate siano in grado di divulgare materiale per le chiavi o di scegliere materiale per le chiavi da origini casuali non sufficienti.
-   Le applicazioni non possono specificare i dettagli delle operazioni di crittografia. L'interfaccia CSP consente a un'applicazione di scegliere un algoritmo di crittografia o di firma, ma l'implementazione di ogni operazione di crittografia viene eseguita dal CSP.
-   Le applicazioni non gestiscono le [*credenziali*](../secgloss/c-gly.md) utente o altri dati di autenticazione utente. L'autenticazione utente viene eseguita dal CSP; quindi, i CSP futuri con funzionalità di autenticazione avanzata, ad esempio gli input biometrici, funzioneranno senza dover modificare il modello di autenticazione dell'applicazione.

Come minimo, un CSP è costituito da una libreria a collegamento dinamico (DLL) e da un [*file di firma*](../secgloss/s-gly.md). Il file della firma è necessario per garantire che [*CryptoAPI*](../secgloss/c-gly.md) riconosca il CSP. CryptoAPI convalida periodicamente questa firma per assicurarsi che vengano rilevate eventuali manomissioni del CSP.

Alcuni DSN possono implementare una parte delle funzionalità in un servizio separato da indirizzi chiamato tramite RPC locale o in hardware chiamato tramite un driver di dispositivo di sistema. Isolando le operazioni globali di crittografia e stato di chiave in un servizio separato dall'indirizzo o nell'hardware, le chiavi e le operazioni non sono sicure per la manomissione in uno spazio dati dell'applicazione.

Non è consigliabile che le applicazioni utilizzino gli attributi specifici di un CSP specifico. Ad esempio, il provider di crittografia di base Microsoft (fornito con CryptoAPI) supporta le chiavi di sessione a 40 bit e le chiavi pubbliche a 512 bit. Le applicazioni che modificano queste chiavi devono evitare presupposti sulla quantità di memoria necessaria per archiviare queste chiavi perché l'applicazione potrebbe non riuscire se viene utilizzato un CSP diverso. Le applicazioni ben scritte devono funzionare con una varietà di CSP.

Per informazioni dettagliate sui tipi di provider del servizio di crittografia e sui DSN predefiniti che possono essere utilizzati con CryptoAPI, vedere [tipi di provider](cryptographic-provider-types.md) del servizio di crittografia e provider del [servizio di crittografia Microsoft](microsoft-cryptographic-service-providers.md).

 

 
