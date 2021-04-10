---
title: Personalizzazione del progetto di esempio
description: Personalizzazione del progetto di esempio
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player Online Stores, personalizzazione di progetti di esempio
- negozi online, personalizzazione di progetti di esempio
- digitare 2 archivi online, personalizzazione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- personalizzazione di progetti di esempio
- esempi, digitare 2 archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955757"
---
# <a name="customizing-the-sample-project"></a>Personalizzazione del progetto di esempio

Quando si crea un archivio online personalizzato, è necessario modificare le implementazioni dei metodi seguenti nel file denominato Progettoutente. cpp:

-   **CYourProject:: allowPlay**. Usare questa funzione per applicare le regole business per consentire la riproduzione di contenuto protetto.
-   **CYourProject:: Allow cdburn**. Usare questa funzione per applicare le regole business per consentire agli utenti di copiare il contenuto protetto in un CD.
-   **CYourProject:: allowPDATransfer**. Usare questa funzione per applicare le regole business per consentire agli utenti di trasferire contenuti protetti a un dispositivo portatile.
-   **CYourProject:: startBackgroundProcessing**. Usare questa funzione per avviare le attività di elaborazione in background necessarie. È possibile, ad esempio, usarlo come opportunità per verificare la presenza di licenze scadute.
-   **CYourProject::D eviceavailable**. Usare questa funzione per avviare le attività correlate a un dispositivo connesso.
-   **CYourProject::P repareforsync**. Usare questa funzione per eseguire le attività necessarie poco prima di sincronizzare i supporti digitali con il dispositivo.
-   **CYourProject:: serviceEvent**. Utilizzare questa funzione per iniziare e terminare le attività che si desidera eseguire quando lo Store online è quello attivo.
-   **CYourProject:: stopBackgroundProcessing**. Usare questa funzione per arrestare le attività di elaborazione in background avviate quando Windows Media Player denominato **CYourProject:: startBackgroundProcessing**.

## <a name="working-with-media-and-playlist-objects"></a>Utilizzo di oggetti multimediali e playlist

Il metodo **allowPlay** fornisce un puntatore all'interfaccia **IWMPMedia** come parametro. Questa interfaccia è l'interfaccia di Windows Media Player che rappresenta gli oggetti multimediali. Chiamando i metodi su questa interfaccia, è possibile usare gli attributi e le proprietà di un singolo elemento multimediale.

I metodi **allowCDBurn** e **allowPDATransfer** forniscono un puntatore all'interfaccia **IWMPPlaylist** come parametro. Questa interfaccia è l'interfaccia di Windows Media Player che rappresenta gli oggetti playlist. Chiamando i metodi su questa interfaccia, è possibile usare gli attributi e le proprietà di una playlist, aggiungere elementi a una playlist o rimuovere elementi da una playlist.

Per informazioni su come rimuovere un elemento da una playlist a livello di codice, vedere l'implementazione di **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**. Per altre informazioni sull'uso di oggetti multimediali e playlist, vedere il [modello a oggetti del lettore per i linguaggi di scripting](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Codice che può essere rimosso

Probabilmente si vorrà rimuovere il codice che apre le finestre di dialogo perché è improbabile che gli utenti decidano quali elementi multimediali possono essere riprodotti o copiati. Da Progettoutente. h rimuovere il codice seguente:

-   Dichiarazione di **CAllowBaseDialog**.
-   Dichiarazione di **CAllowBurnDialog**.
-   Dichiarazione di **CAllowTransferDialog**.

Da Progettoutente. cpp rimuovere il codice seguente:

-   Implementazione di **CAllowBaseDialog <T> :: OnInitDialog**.
-   Implementazione di **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del plug-in per un negozio online di tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




