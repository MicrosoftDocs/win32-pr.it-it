---
description: Per compilare applicazioni Tablet PC in C e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly della libreria gestita di \# Tablet PC. In questo modo è possibile accedere al modello a oggetti gestito e ai controlli.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Libreria e controlli gestiti (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b4096ba54d3cd882b3ee50469d94792b4a46ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884280"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Libreria e controlli gestiti (Tablet PC)

Per compilare applicazioni Tablet PC in C e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly della libreria gestita di \# Tablet PC. In questo modo è possibile accedere al modello a oggetti gestito e ai controlli.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# e Visual Basic.NET

In Windows Vista gli assembly della libreria gestita di Tablet PC vengono installati per impostazione predefinita in due directory:

-   &lt;&gt;systemdrive: Programmi File comuni Directory Microsoft Shared \\ \\ \\ \\ Ink
-   &lt;&gt;systemdrive: Programmi Microsoft SDK Windows Bin \\ \\ \\ \\ v6.0 \\

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

 

 

 



