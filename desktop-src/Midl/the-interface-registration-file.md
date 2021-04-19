---
title: File di registrazione dell'interfaccia
description: Il file di registrazione dell'interfaccia raccoglie informazioni che consentono di registrare le interfacce COM in un file DLL o EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- file di registrazione dell'interfaccia MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299754"
---
# <a name="the-interface-registration-file"></a>File di registrazione dell'interfaccia

Il file di registrazione dell'interfaccia raccoglie informazioni che consentono di registrare le interfacce COM in un file DLL o EXE. Il file di registrazione dell'interfaccia è diverso dagli altri file generati perché può raccogliere informazioni dalla compilazione di più file IDL diversi. Ogni compilatore MIDL eseguito per le interfacce COM cerca innanzitutto un file dlldata. c esistente e, se il file non viene trovato, viene creato un nuovo file dlldata. c. Se viene trovato un file dlldata. c, le informazioni sull'IDL corrente vengono aggiunte (se assenti) o sostituite.

Il file di registrazione dell'interfaccia viene generato o aggiornato in modo sicuro in un ambiente multiprocessore perché le compilazioni parallele MIDL non possono scrivere nel file nello stesso momento. Poiché qualsiasi file dlldata. c può essere contrassegnato come di sola lettura dall'ambiente di compilazione o dall'utente, il compilatore MIDL implementa un approccio di timeout per l'attesa di un file che non può essere aperto e genera un messaggio di errore appropriato se il timeout scade.

Il nome predefinito per il file di registrazione dell'interfaccia generato da un file di input è dlldata. c. L'opzione del compilatore MIDL [**/dlldata**](-dlldata.md) può essere usata per eseguire l'override del nome predefinito del file. L'override del nome predefinito del file di registrazione dell'interfaccia è particolarmente utile quando alcuni file IDL inclusi in un file binario comune si trovano in directory diverse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione e registrazione di una DLL proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 