---
title: Informazioni sull'API Image Mastering
description: Questa documentazione è incentrata su una descrizione dell'implementazione Adaptec di IMAPI per Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- API di mastering delle immagini IMAPI, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb16ab8c542e7c4686c7a3f4d027169a520495a8d3fab9927f11ed974deeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451906"
---
# <a name="about-the-image-mastering-api"></a>Informazioni sull'API Image Mastering

Questa documentazione è incentrata su una descrizione dell'implementazione Adaptec di IMAPI per Microsoft (IMAPIv1). Di conseguenza, le descrizioni dei quattro oggetti COM principali e delle relative interfacce sono incluse in questo documento. I quattro oggetti principali sono i seguenti: **MSDiscMasterObj**, **MSDiscRecorderObj**, **MSDiscStashObj** e **MSEngineObj**.

Possono essere presenti più **oggetti MSDiscMasterObj** di cui è stata creata un'istanza in un sistema, ma solo un'applicazione può accedere a un registratore alla volta. **MSDiscMasterObj** implementa più interfacce, come illustrato nel diagramma oggetti seguente.

![msdiscmasterobj implementa più interfacce](images/imapi.png)

Le applicazioni usano [**l'interfaccia IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) per eseguire le attività seguenti:

-   Aprire IMAPI
-   Enumerare i formati supportati (Joliet e Redbook)
-   Selezionare un formato
-   Ottenere un elenco di registratori
-   Selezionare un registratore
-   Avviare una masterizzazione

Le [**interfacce IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) vengono restituite a un'applicazione tramite l'interfaccia [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) quando viene selezionato un formato. Queste interfacce controllano rispettivamente il contenuto di un disco audio o di dati. Non è previsto che ogni applicazione comprendi le interfacce di formato specifiche. Le applicazioni possono accedere alle proprietà generiche **dell'interfaccia IJolietDiscMaster,** ad esempio il nome del volume o il nome file legacy.

**Gli oggetti MSDiscRecorderObj** sono accessibili tramite [**l'interfaccia IDiscRecorder.**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) Ogni dispositivo CD-R o CD-RW compatibile con IMAPI ha un oggetto **MSDiscRecorderObj** corrispondente. Un'applicazione usa puntatori **all'interfaccia IDiscRecorder** su tali oggetti per selezionare il dispositivo che verrà usato da IMAPI per registrare un CD. Inoltre, le applicazioni possono accedere alle proprietà generiche di un registratore **tramite IDiscRecorder.** Sono incluse proprietà come la velocità del writer o altri parametri di masterizzazione.

Gli oggetti rimanenti, **MSDiscStashObj** e **MSEngineObj,** sono oggetti interni accessibili da IMAPI. Sono menzionati qui solo per chiarire l'architettura IMAPI. **MSDiscStashObj** rappresenta (tramite l'interfaccia **IDiscStash)** un file non elaborato di dimensioni fino a 800 MB usato da **MSDiscMasterObj** per creare immagini audio o dischi di dati da riprodurre. Lo stash viene passato a **MSEngineObj** (tramite **l'interfaccia IMSEngineEngine)** quando viene richiesta una masterizzazione dal motore di livello inferiore. **L'oggetto MSEngineObj** prevede che il contenuto dello stash sia in un formato noto. In questo senso, **MSDiscMasterObj** e **MSEngineObj** hanno un contratto relativo al contenuto dello stash.

 

 




