---
description: In questa sezione viene descritto come configurare l'ambiente per l'utilizzo delle librerie COM della piattaforma Tablet PC in C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Libreria COM e controlli ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305689"
---
# <a name="com-library-and-activex-controls"></a>Libreria COM e controlli ActiveX

In questa sezione viene descritto come configurare l'ambiente per l'utilizzo delle librerie COM della piattaforma Tablet PC in C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Per compilare applicazioni per Tablet PC in Visual C++, è necessario aggiornare le variabili di ambiente di sistema, impostare le opzioni di directory per Visual Studio e accedere alle interfacce di Tablet PC nel progetto.

Per aggiornare le variabili di ambiente, seguire le istruzioni fornite dal Windows SDK per aggiungere le variabili di ambiente a Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Accesso alle interfacce di Tablet PC

Per accedere alle interfacce di Tablet PC, è necessario includere i file Msinkaut. h e Msinkaut \_ i. c nel progetto.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



È anche possibile usare la direttiva import seguente anziché le \# istruzioni include elencate in precedenza.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Per accedere alle interfacce InkAnalysis, è necessario includere i file IACom. h e IACom \_ i. c nel progetto.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



È anche possibile usare la direttiva import seguente anziché le \# istruzioni include elencate in precedenza.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Per accedere alle interfacce [**InkDivider**](inkdivider-class.md) , è necessario includere \_ i file msinkaut15 i. c e msinkaut15. h nel progetto.

> [!Note]  
> InkDivider è stato sostituito dalle API di analisi dell'input penna.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



È anche possibile usare la direttiva import seguente anziché le \# istruzioni include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Per accedere alle interfacce [**PenInputPanel**](peninputpanel-class.md) , è necessario includere \_ i file PenInputPanel i. c e PenInputPanel. h nel progetto.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



È anche possibile usare la direttiva import seguente anziché le \# istruzioni include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> Le API PenInputPanel sono state sostituite in Windows Vista dalle nuove interfacce del pannello di input di testo.

 

Per accedere alle interfacce di controllo [InkEdit](inkedit-control-reference.md) , è necessario includere i file inchiostrate. h e inchiostrati \_ i. c nel progetto.


```C++
#include <inked.h>
#include <inked_i.c>
```



In alternativa, è possibile \# importare il file di InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



