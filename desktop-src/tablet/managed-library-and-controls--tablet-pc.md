---
description: Per compilare applicazioni per Tablet PC in C \# e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly di librerie gestite da Tablet PC. Consente di accedere al modello a oggetti gestito e ai controlli.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Libreria e controlli gestiti (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316822"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Libreria e controlli gestiti (Tablet PC)

Per compilare applicazioni per Tablet PC in C \# e Visual Basic .NET, il progetto in Microsoft Visual Studio .NET deve includere un riferimento agli assembly di librerie gestite da Tablet PC. Consente di accedere al modello a oggetti gestito e ai controlli.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# e visual Basic.NET

In Windows Vista, gli assembly della libreria gestita di Tablet PC vengono installati per impostazione predefinita in due directory:

-   <systemdrive>: \\ Programmi file \\ comuni \\ Microsoft Shared \\ Ink directory
-   <systemdrive>: \\ Programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin

Per aggiungere un riferimento alle librerie gestite dalla piattaforma Tablet PC in Microsoft Visual Studio .NET:

1.  Aprire il progetto Visual Studio .NET.
2.  Scegliere **Aggiungi riferimento** dal menu **Progetto**.
3.  Nella scheda **.NET** della finestra di dialogo **Aggiungi riferimento** selezionare l' **API Microsoft Tablet PC** nell'elenco componenti.
4.  Fare clic su **Seleziona** e quindi su **OK**.

Per aggiungere un riferimento alle API di analisi dell'input penna in Visual Studio .NET:

1.  Aprire il progetto Microsoft Visual Studio .NET.
2.  Scegliere **Aggiungi riferimento** dal menu **Progetto**.
3.  Nella scheda **.NET** della finestra di dialogo **Aggiungi riferimento** , nell'elenco componenti selezionare **libreria gestita di analisi dell'input penna Microsoft Tablet PC**.
4.  Fare clic su **Seleziona** e quindi su **OK**.

> [!Note]  
> Quando si compilano applicazioni che usano Microsoft. Ink in Visual Studio 2005, è necessario selezionare **progetto**, selezionare **Proprietà**, selezionare **Compila** e impostare target piattaforma = x86. Questa opzione non è disponibile nei prodotti Microsoft Visual Studio Express.

 

 

 



