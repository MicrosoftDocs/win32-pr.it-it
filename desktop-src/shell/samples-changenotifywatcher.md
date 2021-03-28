---
description: Viene illustrato come ascoltare le notifiche di modifica della shell su una cartella o un elemento nello spazio dei nomi di Esplora risorse.
title: Esempio di Watcher per notifiche di modifica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232712"
---
# <a name="change-notify-watcher-sample"></a>Esempio di Watcher per notifiche di modifica

Viene illustrato come ascoltare le notifiche di modifica della shell su una cartella o un elemento nello spazio dei nomi di Esplora risorse.

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
| GitHub  | [Esempio ChangeNotifyWatcher](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ChangeNotifyWatcher** .
2.  Immettere `msbuild ChangeNotifyWatcher.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **ChangeNotifyWatcher** .
2.  Fare doppio clic sull'icona per il file ChangeNotifyWatcher. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Al prompt dei comandi digitare `ChangeNotifyWatcher.exe`. In alternativa, in Esplora risorse fare doppio clic sull'icona per ChangeNotifyWatcher.exe.
3.  Per illustrare l'effetto, gli ID del modello utente dell'applicazione (AppUserModelIDs) selezionano una cartella da controllare facendo clic su **"pick..."** o usando il trascinamento della selezione in una cartella da una finestra di Esplora risorse nella visualizzazione elenco dell'esempio.

 

 



