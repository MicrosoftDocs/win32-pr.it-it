---
title: Strumento di Command-Line MkTypLib
description: MkTypLib è un'applicazione della riga di comando che elabora un file IDL per produrre una libreria dei tipi. Può essere usato anche per generare un file di intestazione C o C++.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b712ed8220dd609dd3ba189bdac6b5ee11d2805f26ff5a1f146c20f17c1f8ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047939"
---
# <a name="mktyplib-command-line-tool"></a>Strumento di Command-Line MkTypLib

\[Lo Mktyplib.exe è obsoleto. In alternativa, usare il compilatore MIDL. Se è necessaria la compatibilità con le versioni precedenti dei programmi di Automazione, usare il compilatore MIDL con **l'opzione /mktyplib203.**\]

MkTypLib è un'applicazione della riga di comando che elabora un file IDL per produrre una libreria dei tipi. Può essere usato anche per generare un file di intestazione C o C++.

Per generare una libreria dei tipi da un file ODL:

-   Al prompt dei comandi eseguire il comando seguente:

    **mktyplibÂ **_filename_

    dove *filename* è il nome del file ODL.

MkTypLib supporta anche diversi parametri facoltativi. Per un elenco completo, eseguire la riga di comando seguente:

**mktyplib /?**

Poiché MkTypLib è un'applicazione obsoleta, non può analizzare file IDL o file con interfacce definite all'esterno di [**un'istruzione di**](/windows/desktop/Midl/library) libreria. Per altre informazioni, vedere [Differenze tra MIDL e MkTypLib.](/windows/desktop/Midl/differences-between-midl-and-mktyplib)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in C++](translating-to-c--.md)
</dt> </dl>

 

 