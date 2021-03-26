---
description: Viene illustrato come creare una Jump List personalizzata per un'applicazione, tra cui l'aggiunta di una categoria e attività personalizzate.
title: Esempio di jump list personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232710"
---
# <a name="custom-jump-list-sample"></a>Esempio di jump list personalizzata

Viene illustrato come creare una Jump List personalizzata per un'applicazione, tra cui l'aggiunta di una categoria e attività personalizzate.

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
| GitHub  | [Esempio CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **CustomJumpList** .
2.  Immettere `msbuild CustomJumpListSample.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **CustomJumpList** .
2.  Fare doppio clic sull'icona per il file CustomJumpListSample. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `CustomJumpListSample.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per CustomJumpListSample.exe.
3.  Questo esempio deve essere eseguito come amministratore alla prima esecuzione, in modo da poter installare le registrazioni dei tipi di file necessarie. Dopo la registrazione dei tipi di file, l'esempio può essere eseguito come utente standard.
4.  Scegliere Opzioni dal menu nell'applicazione di esempio per vedere come influiscono sulla Jump List dell'applicazione nella barra delle applicazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ID modello utente applicazione (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



