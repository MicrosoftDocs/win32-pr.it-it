---
title: Documenti e periferiche per documenti
description: Windows 7 offre agli sviluppatori una piattaforma affidabile per l'utilizzo di documenti e l'integrazione di periferiche per i documenti.
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047147"
---
# <a name="documents-and-document-peripherals"></a>Documenti e periferiche per documenti

Windows 7 offre agli sviluppatori una piattaforma affidabile per l'utilizzo di documenti e l'integrazione di periferiche per i documenti. In Windows Vista sono state introdotte due nuove tecnologie di archiviazione e documenti: XML Paper Specification (XPS) e Open Packaging Conventions (OPC). Queste tecnologie, disponibili solo in Windows Vista per gli sviluppatori di applicazioni con codice gestito tramite il Framework di Microsoft .NET, sono ora disponibili in Windows 7software Development Kit (SDK) per l'uso da parte degli sviluppatori di codice non gestito.

## <a name="open-packaging-conventions"></a>Open Packaging Conventions

Windows 7 supporta tutti i formati di file OPC, inclusi quelli di Microsoft e quelli di terze parti. OPC è un componente delle specifiche internazionali di Office Open XML (OOXML) definite tramite *ISO/IEC DIS 29500* e *ECMA-376*. In base al formato di file *zip* , OPC consente alle applicazioni di archiviare una combinazione di elementi di dati all'interno di un unico file di pacchetto. Gli sviluppatori di applicazioni possono utilizzare le API per la creazione di *pacchetti* in Windows 7 per creare, leggere e modificare più elementi dati nei file basati su OPC.

Utilizzando le API per la creazione di *pacchetti* in Windows 7, gli sviluppatori possono creare nuovi formati di pacchetto per soddisfare i requisiti di archiviazione dei dati specifici dell'applicazione.

Le firme digitali *X509* sono supportate anche dalle API per la creazione di *pacchetti*. Gli sviluppatori possono usare le funzionalità di firma digitale per firmare e convalidare parti selezionate di un pacchetto OPC o dell'intero pacchetto. Le applicazioni possono fornire ai propri documenti un livello aggiuntivo di sicurezza usando le firme digitali per rilevare quando il contenuto di un file basato su OPC è stato modificato dopo la firma del file. Vedere [Panoramica di Open Packaging Conventions](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview).

## <a name="xps-documents"></a>Documenti XPS

Gli sviluppatori di applicazioni Windows possono creare applicazioni che producono documenti XPS con Windows 7. Questo consente loro di integrarsi strettamente con l'ecosistema di periferiche del documento (dispositivi come scanner e stampanti) e di usare un documento elettronico sicuro per supportare la pubblicazione e l'archiviazione.

Nelle versioni precedenti di Windows, XPS non era supportato per gli sviluppatori di Microsoft Win32. XPS è stato introdotto in Windows Vista, ma la superficie dell'API è stata limitata agli sviluppatori .NET che utilizzano codice gestito. Con Windows 7, gli sviluppatori Win32 possono utilizzare le nuove API dei *documenti* XPS per ridurre la quantità di lavoro necessaria quando si utilizza XPS. Poiché XPS è la base della nuova piattaforma di stampa Windows, questo è un vantaggio significativo.

Nelle versioni precedenti di Windows, l'accesso al percorso di stampa XPS dalle applicazioni Win32 era limitato ai caratteri di escape del driver. Questo ha ridotto significativamente l'utilità del percorso di stampa per gli sviluppatori che non utilizzano codice gestito. Per gli sviluppatori Win32, la nuova API di *stampa* XPS riduce significativamente la quantità di lavoro necessaria per trarre vantaggio dai vantaggi del percorso di stampa XPS ed elimina la necessità di codice di stampa parallela.

Gli sviluppatori di applicazioni possono utilizzare documenti XPS per condividere e archiviare contenuto come carta elettronica in un formato altamente fedele, efficiente e affidabile. Analogamente a Windows Vista, il percorso di stampa in Windows 7 è basato sul formato XPS per fornire funzionalità di stampa avanzate. Le API dei documenti XPS in Windows 7 offrono agli sviluppatori la possibilità di creare, accedere e modificare facilmente i documenti XPS. Vedere la [Guida alla programmazione di documenti XPS](/previous-versions//dd372978(v=vs.85)).

![Visualizzatore XPS](images/windows7-devguide-xpsviewer.jpg)

Gli sviluppatori di applicazioni Windows possono creare applicazioni che producono documenti XPS con Windows 7

 

 