---
title: Stringhe di formato delle procedure
description: Di seguito è riportata una descrizione della stringa di formato completa. Assembla tutti i livelli correlati alle diverse fasi dell'evoluzione dell'interprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963318"
---
# <a name="procedure-format-strings"></a>Stringhe di formato delle procedure

Di seguito è riportata una descrizione della stringa di formato completa. Assembla tutti i livelli correlati alle diverse fasi dell'evoluzione dell'interprete.

## <a name="procedure-descriptor-overview"></a>Panoramica del descrittore di procedure

Un descrittore di routine è costituito dai descrittori di intestazione e dai descrittori di parametro. La descrizione dello stile [**-OI**](/windows/desktop/Midl/-oi) è considerata obsoleta in termini di utilizzo comune nella programmazione RPC corrente. **-OIF** è considerato più aggiornato.

## <a name="the-oi-style-description"></a>Descrizione dello stile-OI

Questa descrizione è costituita dagli elementi seguenti:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

L'intestazione avrà da 6 a 16 byte.

La descrizione completa viene generata durante la compilazione in modalità [**-OI**](/windows/desktop/Midl/-oi) . In [**-modalità sistema operativo**](/windows/desktop/Midl/-os) vengono generati solo i descrittori di parametro, che vengono usati per la conversione. L'interprete di selezione USA descrittori di parametri di stile obsoleti.

## <a name="the-oif-style-description"></a>Descrizione dello stile – OIF

La descrizione è costituita dagli elementi seguenti:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

Il descrittore di intestazione di stile [**– OIF**](/windows/desktop/Midl/-oi) è costituito da

La descrizione dello stile – OIF viene generata durante la compilazione in modalità [**– OIF**](/windows/desktop/Midl/-oi) o **– Oicf** del compilatore.

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Alcune funzionalità più recenti come pipe, Async e [**/robust**](/windows/desktop/Midl/-robust) forzano la modalità [**– Oicf**](/windows/desktop/Midl/-oi) del compilatore, quando vengono usate.

## <a name="the-extended-oif-description"></a>Descrizione estesa-OIF

La descrizione è costituita dagli elementi seguenti:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 