---
description: Viene illustrato come creare un verbo che opera su elementi e contenitori della shell che riproduce elementi o aggiunge elementi a una coda.
title: Esempio di verbo del lettore
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231924"
---
# <a name="player-verb-sample"></a>Esempio di verbo del lettore

Viene illustrato come creare un verbo che opera su elementi e contenitori della shell che riproduce elementi o aggiunge elementi a una coda. Questo esempio è particolarmente utile per le applicazioni multimediali.

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio PlayerVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **PlayerVerbSample** .
2.  Immettere `msbuild PlayerVerbSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **PlayerVerbSample** .
2.  Fare doppio clic sull'icona per il file PlayerVerbSample. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `PlayerVerbSample.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per PlayerVerbSample.exe.
3.  Selezionare `Register Verbs` nella finestra di dialogo **Sample verbi Player** .
4.  Fare clic con il pulsante destro del mouse su elementi immagine (file, cartella o stack) in Esplora risorse per aggiungerli a una coda o riprodurli nell'applicazione di esempio. Usare gli elementi musicali quando si modifica l'esempio per lavorare con musica.

 

 



