---
description: Illustra come creare una categoria personalizzata Jump List un'applicazione, inclusa l'aggiunta di una categoria e di attività personalizzate.
title: Esempio di jump list personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb6f5db0b9576f360abcbaacb8a8a5a291d3dbe07754281954ea585d3ebe965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968830"
---
# <a name="custom-jump-list-sample"></a>Esempio di jump list personalizzata

Illustra come creare una categoria personalizzata Jump List un'applicazione, inclusa l'aggiunta di una categoria e di attività personalizzate.

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

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto CustomJumpList.**
2.  Immettere `msbuild CustomJumpListSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto CustomJumpList.**
2.  Fare doppio clic sull'icona per il file CustomJumpListSample.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `CustomJumpListSample.exe` . In alternativa, in Windows Explorer fare doppio clic sull'icona per CustomJumpListSample.exe.
3.  Questo esempio deve essere eseguito come amministratore la prima volta che viene eseguito in modo da poter installare le registrazioni dei tipi di file necessarie. Dopo aver registrato i tipi di file, l'esempio può essere eseguito come utente standard.
4.  Selezionare le opzioni dal menu nell'applicazione di esempio per vedere in che modo influiscono sul Jump List dell'applicazione nella barra delle applicazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelID)](appids.md)
</dt> </dl>

 

 



