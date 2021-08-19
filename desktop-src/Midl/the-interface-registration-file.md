---
title: File di registrazione dell'interfaccia
description: Il file di registrazione dell'interfaccia raccoglie informazioni utili per la registrazione delle interfacce COM in pacchetto in un file DLL o EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- file di registrazione dell'interfaccia MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a5541a5e60b1903364236f86dcf1845a5e1ac153fc91b47bacf9f553a9a109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806179"
---
# <a name="the-interface-registration-file"></a>File di registrazione dell'interfaccia

Il file di registrazione dell'interfaccia raccoglie informazioni utili per la registrazione delle interfacce COM in pacchetto in un file DLL o EXE. Il file di registrazione dell'interfaccia è diverso da altri file generati perché può raccogliere informazioni dalla compilazione di diversi file IDL diversi. Ogni esecuzione del compilatore MIDL per le interfacce COM cerca prima un file dlldata.c esistente e, se il file non viene trovato, viene creato un nuovo file dlldata.c. Se viene trovato un file dlldata.c, le informazioni sull'IDL corrente vengono aggiunte (se assenti) o sostituite.

Il file di registrazione dell'interfaccia viene generato o aggiornato in modo sicuro in un ambiente multiprocessore perché alle compilazioni MIDL parallele non è consentito scrivere nel file contemporaneamente. Poiché qualsiasi file dlldata.c può essere contrassegnato come di sola lettura dall'ambiente di compilazione o dall'utente, il compilatore MIDL implementa un approccio di timeout per l'attesa di un file che non può aprire e genera un messaggio di errore appropriato se il timeout scade.

Il nome predefinito per il file di registrazione dell'interfaccia generato da un file di input è dlldata.c. L'opzione del compilatore MIDL [**/dlldata**](-dlldata.md) può essere usata per eseguire l'override del nome predefinito del file. L'override del nome predefinito del file di registrazione dell'interfaccia è particolarmente utile quando alcuni file IDL in pacchetto in un file binario comune si trovano in directory diverse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione e registrazione di una DLL proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 