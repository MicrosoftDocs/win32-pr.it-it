---
title: Generazione di una libreria dei tipi con MIDL
description: L'elemento di primo livello della sintassi ODL è l'istruzione library (blocco di libreria).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language MIDL , attività, generazione di una libreria dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d9084631dc30eb1cff7f61f6f3f090f95bb92cff357b3902cb0959f2c4142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013849"
---
# <a name="generating-a-type-library-with-midl"></a>Generazione di una libreria dei tipi con MIDL

L'elemento di primo livello della sintassi ODL è l'istruzione library (blocco di libreria). Ogni altra istruzione ODL, ad eccezione degli attributi applicati all'istruzione library, deve essere definita all'interno del blocco di libreria. Quando il compilatore MIDL visualizza un blocco di libreria, genera una libreria dei tipi in modo molto identico a MkTypLib. Con alcune eccezioni, descritte in Differenze tra MIDL e [MKTYPLIB,](differences-between-midl-and-mktyplib.md)le istruzioni all'interno del blocco di libreria devono seguire la stessa sintassi del linguaggio ODL e MkTypLib.

> [!Note]  
> Lo Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL.

 

È possibile applicare attributi ODL agli elementi definiti all'interno o all'esterno del blocco di libreria. Questi attributi non hanno alcun effetto all'esterno del blocco di libreria, a meno che all'elemento a cui vengono applicati non venga fatto riferimento all'interno del blocco di libreria. Le istruzioni all'interno del blocco di libreria possono fare riferimento a un elemento esterno usandolo come tipo di base, ereditando da esso o facendo riferimento a esso in una riga come illustrato:

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

Se si fa riferimento a un elemento definito all'esterno del blocco di libreria all'interno del blocco di libreria, la relativa definizione verrà inserita nella libreria dei tipi generata. Il compilatore MIDL considera le istruzioni all'esterno di un blocco di libreria come un file IDL tipico e analizza tali istruzioni come sempre fatto. In genere, ciò significa generare stub in linguaggio C per un'applicazione RPC.

Per altre informazioni sulla sintassi generale per un file ODL, vedere [Sintassi di file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).

 

 