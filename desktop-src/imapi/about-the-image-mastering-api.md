---
title: Informazioni sull'API per la creazione di immagini master
description: Questa documentazione è incentrata su una descrizione dell'implementazione di Adaptec di IMAPi per Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- API di master delle immagini IMAPi, descritta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db1dc7846d2e47483abf2ca8856d593b874467f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104553909"
---
# <a name="about-the-image-mastering-api"></a>Informazioni sull'API per la creazione di immagini master

Questa documentazione è incentrata su una descrizione dell'implementazione di Adaptec di IMAPi per Microsoft (IMAPIv1). Di conseguenza, in questo documento sono incluse le descrizioni dei quattro oggetti COM principali e delle relative interfacce. I quattro oggetti principali sono i seguenti: **MSDiscMasterObj**, **MSDiscRecorderObj**, **MSDiscStashObj** e **MSBurnEngineObj**.

Possono essere presenti più oggetti **MSDiscMasterObj** di cui è stata creata un'istanza in un sistema, ma solo un'applicazione può accedere a un registratore alla volta. **MSDiscMasterObj** implementa più interfacce, come illustrato nel diagramma di oggetti seguente.

![msdiscmasterobj implementa più interfacce](images/imapi.png)

Le applicazioni utilizzano l'interfaccia [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) per eseguire le attività seguenti:

-   Apri IMAPi
-   Enumerare i formati supportati (Joliet e Redbook)
-   Selezionare un formato
-   Ottenere un elenco di record
-   Selezionare un registratore
-   Avvia un'ustione

Le interfacce [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) vengono restituite a un'applicazione tramite l'interfaccia [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) quando viene selezionato un formato. Queste interfacce controllano rispettivamente il contenuto di un disco dati o audio. Non è previsto che tutte le applicazioni siano in grado di comprendere le interfacce di formato specifiche. Le applicazioni possono accedere alle proprietà generiche dell'interfaccia **IJolietDiscMaster** , ad esempio il nome del volume o il nome del file legacy.

Gli oggetti **MSDiscRecorderObj** sono accessibili tramite l'interfaccia [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) . Ogni dispositivo CD-R o CD-RW compatibile con IMAPi ha un oggetto **MSDiscRecorderObj** corrispondente. Un'applicazione usa i puntatori all'interfaccia **IDiscRecorder** su tali oggetti per selezionare il dispositivo che verrà usato da IMAPI per registrare un CD. Inoltre, le applicazioni possono accedere alle proprietà generiche di un registratore tramite **IDiscRecorder**. Sono incluse proprietà quali la velocità del writer o altri parametri Burn.

Gli oggetti rimanenti, **MSDiscStashObj** e **MSBurnEngineObj**, sono oggetti interni accessibili da IMAPI. Sono citati qui solo per chiarire l'architettura di IMAPi. **MSDiscStashObj** rappresenta (tramite l'interfaccia **IDiscStash** ) un file non elaborato con dimensioni fino a 800 MB utilizzate da **MSDiscMasterObj** per creare immagini audio o dischi dati da masterizzare. Il stash viene passato a **MSBurnEngineObj** (tramite l'interfaccia **IMSBurnEngine** ) quando viene richiesta un'ustione dal motore di livello inferiore. L'oggetto **MSBurnEngineObj** prevede che il contenuto del Stash sia in un formato noto. In questo senso, **MSDiscMasterObj** e **MSBurnEngineObj** hanno un contratto relativo al contenuto del stash.

 

 




