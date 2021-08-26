---
title: Stringhe di formato delle procedure
description: Di seguito è riportata una descrizione completa della stringa di formato. Assembla tutti i livelli correlati alle diverse fasi dell'evoluzione dell'interprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb17434a1c05b66212283237d61ee4492aa23ed0bf1ecca75f1fec1b3ddd784b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019059"
---
# <a name="procedure-format-strings"></a>Stringhe di formato delle procedure

Di seguito è riportata una descrizione completa della stringa di formato. Assembla tutti i livelli correlati alle diverse fasi dell'evoluzione dell'interprete.

## <a name="procedure-descriptor-overview"></a>Cenni preliminari sul descrittore di procedura

Un descrittore di routine è costituito dai descrittori di intestazione e dai descrittori di parametro. La descrizione dello stile [**-Oi**](/windows/desktop/Midl/-oi) è considerata obsoleta, in termini di utilizzo comune nella programmazione RPC corrente. **-Oif è** considerato più corrente.

## <a name="the-oi-style-description"></a>Descrizione dello stile –Oi

Questa descrizione è costituita dai seguenti elementi:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

L'intestazione avrebbe da 6 a 16 byte.

La descrizione completa viene generata durante la compilazione in [**modalità –Oi.**](/windows/desktop/Midl/-oi) In [**modalità –Os**](/windows/desktop/Midl/-os) vengono generati solo i descrittori di parametro, che vengono usati per la conversione. L'interprete pickling usa descrittori di parametri di stile precedente.

## <a name="the-oif-style-description"></a>Descrizione dello stile –Oif

La descrizione è costituita dai seguenti elementi:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

Il descrittore di intestazione di stile [**–Oif**](/windows/desktop/Midl/-oi) è costituito da

La descrizione dello stile –Oif viene generata durante la compilazione in modalità [**–Oif**](/windows/desktop/Midl/-oi) o **-Oicf** del compilatore.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Alcune funzionalità più recenti, ad esempio pipe, async e [**/robust,**](/windows/desktop/Midl/-robust) forzano la modalità [**-Oicf**](/windows/desktop/Midl/-oi) del compilatore, se usata.

## <a name="the-extended-oif-description"></a>Descrizione estesa di –Oif

La descrizione è costituita dai seguenti elementi:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 