---
title: Personalizzazione del modello di Project
description: Personalizzazione del modello di Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player negozi online, personalizzazione di progetti di esempio
- negozi online, personalizzazione di progetti di esempio
- negozi online di tipo 2, personalizzazione di progetti di esempio
- Windows Media Player negozi online, progetti di esempio
- negozi online, progetti di esempio
- negozi online di tipo 2, progetti di esempio
- personalizzazione di progetti di esempio
- esempi,tipo 2 negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdb57327904d81ac85114af0df9037d6c2c054938f16048f6ca72e711063cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902081"
---
# <a name="customizing-the-sample-project"></a>Personalizzazione del modello di Project

Quando si crea il proprio negozio online, è necessario modificare le implementazioni dei metodi seguenti nel file denominato YourProject.cpp:

-   **CYourProject::allowPlay**. Usare questa funzione per applicare le regole business per la riproduzione di contenuto protetto.
-   **CYourProject::allow CDBurn**. Usare questa funzione per applicare le regole di business per consentire agli utenti di copiare contenuto protetto in un CD.
-   **CYourProject::allowPDATransfer**. Usare questa funzione per applicare le regole business per consentire agli utenti di trasferire contenuto protetto in un dispositivo portatile.
-   **CYourProject::startBackgroundProcessing**. Usare questa funzione per avviare le attività di elaborazione in background necessarie. Ad esempio, è possibile usarlo come opportunità per verificare la presenza di licenze scadute.
-   **CYourProject::d eviceAvailable**. Usare questa funzione per avviare tutte le attività correlate a un dispositivo connesso.
-   **CYourProject::p repareForSync**. Usare questa funzione per eseguire le attività necessarie subito prima della sincronizzazione dei supporti digitali nel dispositivo.
-   **CYourProject::serviceEvent**. Usare questa funzione per iniziare e terminare le attività che si desidera eseguire quando il negozio online è quello attivo.
-   **CYourProject::stopBackgroundProcessing**. Usare questa funzione per arrestare le attività di elaborazione in background avviate Windows Media Player **chiamata CYourProject::startBackgroundProcessing**.

## <a name="working-with-media-and-playlist-objects"></a>Uso di oggetti multimediali e playlist

Il **metodo allowPlay** fornisce un puntatore all'interfaccia **IWMPMedia** come parametro. Questa interfaccia è l'Windows Media Player che rappresenta gli oggetti multimediali. Chiamando i metodi su questa interfaccia, è possibile usare gli attributi e le proprietà di un singolo elemento multimediale.

I **metodi allowCDBurn** **e allowPDATransfer** forniscono un puntatore all'interfaccia **IWMPPlaylist** come parametro. Questa interfaccia è l'interfaccia Windows Media Player che rappresenta gli oggetti playlist. Chiamando i metodi su questa interfaccia, è possibile usare gli attributi e le proprietà di una playlist, aggiungere elementi a una playlist o rimuovere elementi da una playlist.

Per informazioni su come rimuovere un elemento da una playlist a livello di codice, vedere l'implementazione di **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**. Per altre informazioni sull'uso di oggetti multimediali e playlist, vedere [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Codice che può essere rimosso

È probabile che si voglia rimuovere il codice che apre le finestre di dialogo perché è improbabile che gli utenti decidono quali elementi multimediali possono essere riprodotti o copiati. Da YourProject.h rimuovere il codice seguente:

-   Dichiarazione di **CAllowBaseDialog**.
-   Dichiarazione di **CAllowSaveDialog**.
-   Dichiarazione di **CAllowTransferDialog**.

Da YourProject.cpp rimuovere il codice seguente:

-   Implementazione di **CAllowBaseDialog <T> ::OnInitDialog**.
-   Implementazione di **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Compilazione del plug-in per uno Store online di tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




