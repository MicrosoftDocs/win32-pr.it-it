---
title: Generazione di una libreria dei tipi con MIDL
description: L'elemento di livello principale della sintassi di FAD è l'istruzione Library (blocco libreria).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft Interface Definition Language MIDL, attività, generazione di una libreria di tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299804"
---
# <a name="generating-a-type-library-with-midl"></a>Generazione di una libreria dei tipi con MIDL

L'elemento di livello principale della sintassi di FAD è l'istruzione Library (blocco libreria). Ogni altra istruzione, ad eccezione degli attributi applicati all'istruzione Library, deve essere definita all'interno del blocco di libreria. Quando il compilatore MIDL rileva un blocco di libreria, genera una libreria dei tipi in modo analogo a quanto accade con MkTypLib. Con alcune eccezioni, descritte in [differenze tra MIDL e MkTypLib](differences-between-midl-and-mktyplib.md), le istruzioni all'interno del blocco di libreria devono seguire la stessa sintassi del linguaggio FAD e mktyplib.

> [!Note]  
> Lo strumento Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL.

 

È possibile applicare gli attributi di FAD agli elementi definiti all'interno o all'esterno del blocco di libreria. Questi attributi non hanno alcun effetto all'esterno del blocco di libreria, a meno che all'elemento a cui viene applicato non venga fatto riferimento all'interno del blocco di libreria. Le istruzioni all'interno del blocco di libreria possono fare riferimento a un elemento esterno utilizzandolo come tipo di base, ereditando da esso oppure facendo riferimento a una riga come illustrato di seguito:

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

Se all'interno del blocco di libreria viene fatto riferimento a un elemento definito all'esterno del blocco di libreria, la relativa definizione verrà inserita nella libreria dei tipi generata. Il compilatore MIDL considera le istruzioni all'esterno di un blocco di libreria come un tipico file IDL e analizza tali istruzioni come è sempre stato fatto. In genere, ciò significa generare stub in linguaggio C per un'applicazione RPC.

Per ulteriori informazioni sulla sintassi generale per un file di FAD, vedere la [sintassi del file FAD](/previous-versions/windows/desktop/automat/odl-file-syntax).

 

 