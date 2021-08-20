---
title: Compilazione MIDL
description: Compilazione MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a94f94122aeeb1f2900c3adec7e567c794f31ee22259f657dfe5e95f3f688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047949"
---
# <a name="midl-compilation"></a>Compilazione MIDL

Dato un file IDL, ad esempio [Example2.idl](anatomy-of-an-idl-file.md), che definisce una o più interfacce COM e una libreria dei tipi, il compilatore MIDL (Midl.exe) genera i file descritti nella tabella seguente come output predefinito.



| Nome file                 | Descrizione                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esempio2.h<br/>    | File di intestazione, contenente le definizioni dei tipi e le dichiarazioni di funzione per tutte le interfacce definite nel file IDL, nonché dichiarazioni di inoltro per le routine chiamate da stub.<br/> |
| Esempio2 \_ p.c<br/> | File proxy/stub, che include i punti di ingresso surrogati sia per i client che per i server.<br/>                                                                                           |
| Esempio2 \_ i.c<br/> | File ID interfaccia, che definisce il GUID per ogni interfaccia specificata nel file IDL.<br/>                                                                                               |
| Esempio2.tlb<br/>  | File di documento composto che contiene informazioni su tipi e oggetti.<br/>                                                                                                                |
| Dlldata.c<br/>     | Contiene i dati necessari per creare una DLL proxy/stub.<br/>                                                                                                                                     |



 

Usare il file di intestazione e tutti i file con estensione c per creare una [DLL proxy](building-and-registering-a-proxy-dll.md) in grado di supportare l'interfaccia se usata sia dalle applicazioni client che dai server oggetti. Quando si crea il file eseguibile per un'applicazione client che usa l'interfaccia, usare il file di intestazione dell'interfaccia (Example2.h) e il file ID interfaccia (Example2 \_ i.c). È possibile scegliere di includere il file della libreria dei tipi come risorsa nel file EXE o DLL oppure di spedirlo come file separato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File generati per un'interfaccia COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Opzioni del compilatore MIDL](midl-compiler-options.md)
</dt> </dl>

 

