---
description: Viene illustrato come aggiungere elementi alla Jump List automatica per un'applicazione, incluso il passaggio tra la visualizzazione delle categorie frequenti e recenti.
title: Esempio di jump list automatica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485564"
---
# <a name="automatic-jump-list-sample"></a>Esempio di jump list automatica

Viene illustrato come aggiungere elementi alla Jump List automatica per un'applicazione, incluso il passaggio tra la visualizzazione delle categorie frequenti e recenti.

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)
-   [Argomenti correlati](#related-topics)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio AutomaticJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AutomaticJumpList** .
2.  Immettere `msbuild AutomaticJumpListSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **AutomaticJumpList** .
2.  Fare doppio clic sull'icona per il file AutomaticJumpListSample. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `AutomaticJumpListSample.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per AutomaticJumpListSample.exe.
3.  Questo esempio deve essere eseguito come amministratore alla prima esecuzione, in modo da poter installare le registrazioni dei tipi di file necessarie. Dopo la registrazione dei tipi di file, l'esempio può essere eseguito come utente standard.
4.  Scegliere Opzioni dal menu nell'applicazione di esempio, inclusa la selezione dei documenti con estensione txt o doc tramite la finestra di dialogo **Apri** per vedere come influiscono sulla Jump List dell'applicazione nella barra delle applicazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



