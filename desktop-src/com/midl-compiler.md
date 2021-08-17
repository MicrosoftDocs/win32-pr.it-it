---
title: Compilatore MIDL
description: Compilatore MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db4afbbe8c7a82f4335855b40e578fe2eea046fa4c7f0560e3e297b559a67ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736430"
---
# <a name="midl-compiler"></a>Compilatore MIDL

Il compilatore MIDL elabora un file IDL per generare una libreria dei tipi e i file di output. Il tipo di file di output generati dal compilatore MIDL dipende dagli attributi specificati nell'elenco di attributi di interfaccia del file IDL.

Se l'elenco di attributi contiene la parola chiave object, il compilatore MIDL genera file di output dell'interfaccia COM: un file proxy di interfaccia, un file di intestazione dell'interfaccia e un file di identificatore univoco globale \[ [](/windows/desktop/Midl/object) \] (GUID) per l'interfaccia. Se il file IDL contiene [**un'istruzione library,**](/windows/desktop/Midl/library) MIDL genera un file di libreria dei tipi con estensione tlb. Se nel file IDL sono presenti interfacce che non hanno la parola chiave object e non sono racchiuse in un'istruzione di libreria, il compilatore MIDL genera i file di output dell'interfaccia appropriati per le chiamate di procedura remota \[  \] (RPC): un file stub del client, un file stub del server  e un file di intestazione. Per altre informazioni, vedere gli argomenti [Definizioni di interfaccia e librerie dei tipi](/windows/desktop/Midl/interface-definitions-and-type-libraries) e [Generazione di una libreria dei tipi con MIDL.](/windows/desktop/Midl/generating-a-type-library-with-midl-2)

Per generare una libreria dei tipi e i file di output da un file IDL:

-   Dal prompt dei comandi eseguire

    **midl** *filename*

    dove *nomefile* è il nome del file IDL.

Il compilatore MIDL supporta anche diversi parametri facoltativi. Per un elenco completo, vedere "MIDL Command-Line Reference" (Informazioni di riferimento sul Command-Line MIDL) nella documentazione di Visual C++ oppure eseguire la riga di comando seguente:

**midl /?**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Interface Definition Language](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> </dl>

 

 