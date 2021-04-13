---
title: Stringhe (RPC)
description: Tre tipi di stringhe e RPC (Remote Procedure Call).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338710"
---
# <a name="strings-rpc"></a>Stringhe (RPC)

Sono disponibili tre tipi di stringhe denotate dalle seguenti sottostringhe finali nel formato carattere.



| Tipo                  | Substring |
|-----------------------|-----------|
| Stringa di caratteri      | CSTRING   |
| Stringa di caratteri wide | WSTRING   |
| Struttura in grado di String | SSTRING   |



 

### <a name="nonconformant-strings"></a>Stringhe non conformi

Un esempio di stringa non conforme è una **\[ stringa \]** in una matrice di dimensioni fisse.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Stringhe conformi

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

–oppure–

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

Il primo formato descrive stringhe comuni, come un argomento di tipo **\[ \] stringa** char \* . Una stringa conforme alle dimensioni ha la seconda descrizione.

La descrizione della conformità \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .

### <a name="structure-strings"></a>Stringhe di struttura

Di seguito è riportata una struttura non conforme in grado di String:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Struttura conforme alle stringhe:

``` syntax
FC_C_SSTRING 
element_size<1>
```

o

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

La seconda descrizione è relativa a una struttura di dimensioni in grado di consentire la stringa.

 

 