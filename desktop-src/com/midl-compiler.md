---
title: Compilatore MIDL
description: Compilatore MIDL
ms.assetid: ce3d40b7-49fd-4689-9100-fdbad4f0c557
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa57131e31e9c6273270a771f9ba862d73bc142
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730634"
---
# <a name="midl-compiler"></a>Compilatore MIDL

Il compilatore MIDL elabora un file IDL per generare una libreria dei tipi e i file di output. Il tipo di file di output generati dal compilatore MIDL dipende dagli attributi specificati nell'elenco di attributi di interfaccia del file IDL.

Se l'elenco di attributi contiene la \[ [](/windows/desktop/Midl/object) \] parola chiave Object, il compilatore MIDL genera i file di output dell'interfaccia com: un file proxy di interfaccia, un file di intestazione dell'interfaccia e un file di identificatore univoco globale (Guid) per l'interfaccia. Se il file IDL contiene un'istruzione [**Library**](/windows/desktop/Midl/library) , MIDL genera un file di libreria dei tipi con l'estensione tlb. Se nel file IDL sono presenti interfacce che non hanno la \[  \] parola chiave Object e non sono incluse in un'istruzione **Library** , il compilatore MIDL genera file di output dell'interfaccia appropriati per le chiamate RPC (Remote Procedure Call), ovvero un file stub del client, un file stub del server e un file di intestazione. Per ulteriori informazioni, vedere gli argomenti [definizioni di interfaccia e librerie dei tipi](/windows/desktop/Midl/interface-definitions-and-type-libraries) e [generazione di una libreria dei tipi con MIDL](/windows/desktop/Midl/generating-a-type-library-with-midl-2).

Per generare una libreria dei tipi e i file di output da un file IDL:

-   Al prompt dei comandi eseguire

     *nome file* MIDL

    dove *filename* è il nome del file IDL.

Il compilatore MIDL supporta inoltre diversi parametri facoltativi. Per un elenco completo, vedere "riferimento a MIDL Command-Line" nella documentazione di Visual C++ o eseguire la riga di comando seguente:

**MIDL/?**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Interface Definition Language](/windows/desktop/Midl/midl-start-page)
</dt> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> </dl>

 

 