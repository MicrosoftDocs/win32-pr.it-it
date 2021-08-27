---
description: Illustra come aggiungere elementi al controllo Jump List per un'applicazione, incluso il passaggio tra la visualizzazione delle categorie Frequente e Recente.
title: Esempio di jump list automatica
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4dcb2146c8db8eda0280b3ff7a34a19faf4ac172036ae7a4e61131b50fde2d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090191"
---
# <a name="automatic-jump-list-sample"></a>Esempio di jump list automatica

Illustra come aggiungere elementi al controllo Jump List per un'applicazione, incluso il passaggio tra la visualizzazione delle categorie Frequente e Recente.

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

| Località      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di AutomaticJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **AutomaticJumpList.**
2.  Immettere `msbuild AutomaticJumpListSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto AutomaticJumpList.**
2.  Fare doppio clic sull'icona per il file AutomaticJumpListSample.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**.

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory che contiene il nuovo eseguibile, usando il prompt dei comandi o Windows Explorer.
2.  Nella riga di comando immettere `AutomaticJumpListSample.exe` . In alternativa, da esplora Windows fare doppio clic sull'icona per AutomaticJumpListSample.exe.
3.  Questo esempio deve essere eseguito come amministratore la prima volta che viene eseguito in modo da poter installare le registrazioni dei tipi di file necessarie. Dopo la registrazione dei tipi di file, l'esempio può essere eseguito come utente standard.
4.  Selezionare le opzioni dal menu nell'applicazione di esempio, inclusa la selezione  di documenti .txt o .doc tramite la finestra di dialogo Apri per vedere in che modo influiscono sulla Jump List dell'applicazione nella barra delle applicazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelID)](appids.md)
</dt> </dl>

 

 



