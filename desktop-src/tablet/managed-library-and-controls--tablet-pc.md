---
description: Per compilare applicazioni Tablet PC in C e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly della libreria gestita di \# Tablet PC. In questo modo è possibile accedere al modello a oggetti gestito e ai controlli.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Libreria e controlli gestiti (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d031a97226d200b99a6d36b42e3e4c43862f5b6ac52203ee4ca08d1e5714f2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031729"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Libreria e controlli gestiti (Tablet PC)

Per compilare applicazioni Tablet PC in C e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly della libreria gestita di \# Tablet PC. In questo modo è possibile accedere al modello a oggetti gestito e ai controlli.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# e Visual Basic.NET

In Windows Vista gli assembly della libreria gestita di Tablet PC vengono installati per impostazione predefinita in due directory:

-   <systemdrive>: \\ Programmi File comuni Directory Microsoft Shared \\ \\ \\ Ink
-   <systemdrive>: \\ Programmi Microsoft SDK Windows bin \\ \\ \\ v6.0 \\

Per aggiungere un riferimento alle librerie gestite della piattaforma Tablet PC in Microsoft Visual Studio .NET:

1.  Aprire il Visual Studio .NET.
2.  Scegliere **Aggiungi riferimento** dal menu **Progetto**.
3.  Nella scheda **.NET** della finestra **di** dialogo Aggiungi riferimento selezionare API Microsoft Tablet PC nell'elenco **dei componenti.**
4.  Fare **clic su** Seleziona e quindi su **OK.**

Per aggiungere un riferimento alle API di analisi input penna in Visual Studio .NET:

1.  Aprire il Microsoft Visual Studio .NET.
2.  Scegliere **Aggiungi riferimento** dal menu **Progetto**.
3.  Nella scheda **.NET della** **finestra** di dialogo Aggiungi riferimento selezionare Libreria gestita di analisi input penna di Microsoft Tablet PC nell'elenco dei **componenti.**
4.  Fare **clic su** Seleziona e quindi su **OK.**

> [!Note]  
> Quando si compilano applicazioni che usano Microsoft.Ink in Visual Studio 2005, è necessario selezionare **Project**, selezionare **Proprietà,** selezionare **Compila** e impostare Piattaforma di destinazione=x86. Questa opzione non è disponibile in Microsoft Visual Studio Express prodotti.

 

 

 



