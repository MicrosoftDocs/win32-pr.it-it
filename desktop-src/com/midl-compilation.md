---
title: Compilazione MIDL
description: Compilazione MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474342"
---
# <a name="midl-compilation"></a>Compilazione MIDL

Dato un file IDL, ad esempio [example2. idl](anatomy-of-an-idl-file.md), che definisce una o più interfacce com e una libreria dei tipi, il compilatore MIDL (Midl.exe) genera i file descritti nella tabella seguente come output predefinito.



| Nome file                 | Descrizione                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2. h<br/>    | Il file di intestazione, che contiene le definizioni di tipo e le dichiarazioni di funzione per tutte le interfacce definite nel file IDL, nonché le dichiarazioni con il nome per le routine chiamate dagli stub.<br/> |
| Example2 \_ p. c<br/> | Il file proxy/stub, che include i punti di ingresso surrogati per i client e per i server.<br/>                                                                                           |
| Example2 \_ i. c<br/> | Il file dell'ID di interfaccia, che definisce il GUID per ogni interfaccia specificata nel file IDL.<br/>                                                                                               |
| Example2. tlb<br/>  | Un file di documento composto che contiene informazioni su tipi e oggetti.<br/>                                                                                                                |
| Dlldata. c<br/>     | Contiene i dati necessari per creare una DLL proxy/stub.<br/>                                                                                                                                     |



 

Utilizzare il file di intestazione e tutti i file con estensione c per [creare una DLL proxy](building-and-registering-a-proxy-dll.md) in grado di supportare l'interfaccia quando viene utilizzata da applicazioni client e da server oggetti. Usare il file di intestazione dell'interfaccia (example2. h) e il file dell'ID di interfaccia (example2 \_ i. c) quando si crea il file eseguibile per un'applicazione client che usa l'interfaccia. È possibile scegliere di includere il file della libreria dei tipi come risorsa nel file EXE o DLL oppure è possibile inviarlo come file separato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File generati per un'interfaccia COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Opzioni del compilatore MIDL](midl-compiler-options.md)
</dt> </dl>

 

