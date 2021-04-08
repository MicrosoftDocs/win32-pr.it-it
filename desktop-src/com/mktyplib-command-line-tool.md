---
title: Strumento Command-Line MkTypLib
description: MkTypLib è un'applicazione della riga di comando che elabora un file IDL per produrre una libreria dei tipi. Può essere usato anche per generare un file di intestazione C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730639"
---
# <a name="mktyplib-command-line-tool"></a>Strumento Command-Line MkTypLib

\[Lo strumento Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL. Se è necessaria la compatibilità con le versioni precedenti dei programmi di automazione, usare il compilatore MIDL con l'opzione **/mktyplib203** .\]

MkTypLib è un'applicazione della riga di comando che elabora un file IDL per produrre una libreria dei tipi. Può essere usato anche per generare un file di intestazione C o C++.

Per generare una libreria dei tipi da un file FAD:

-   Al prompt dei comandi eseguire il comando seguente:

    **mktyplibÂ * * * nomefile*

    dove *filename* è il nome del file FAD.

MkTypLib supporta inoltre diversi parametri facoltativi. Per un elenco completo, eseguire la riga di comando seguente:

**MkTypLib/?**

Poiché MkTypLib è un'applicazione obsoleta, non è in grado di analizzare file o file IDL con interfacce definite all'esterno di un'istruzione di [**libreria**](/windows/desktop/Midl/library) . Per altre informazioni, vedere [differenze tra MIDL e MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> </dl>

 

 