---
title: Stringhe (RPC)
description: Tre tipi di stringhe e RPC (Remote Procedure Call).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15467ed5a1425443cbc5a53cf35aba71725c5db68c542c292af38eb0d238cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924837"
---
# <a name="strings-rpc"></a>Stringhe (RPC)

Nel carattere di formato sono presenti tre tipi di stringhe con le sottostringa finali seguenti.



| Tipo                  | Substring |
|-----------------------|-----------|
| Stringa di caratteri      | Cstring   |
| Stringa di caratteri wide | WSTRING   |
| Struttura in grado di usare stringhe | SSTRING   |



 

### <a name="nonconformant-strings"></a>Stringhe non conformi

Un esempio di stringa non conforme è una **\[ stringa in \]** una matrice di dimensioni fisse.

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

Il primo formato descrive le stringhe comuni, ad esempio un **\[ argomento string \]** \* char. Una stringa conforme alle dimensioni ha la seconda descrizione.

La descrizione della<> è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno utilizzato.

### <a name="structure-strings"></a>Stringhe di struttura

Di seguito è riportata una struttura non conforme a stringa:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Struttura conforme a string-able:

``` syntax
FC_C_SSTRING 
element_size<1>
```

–or:

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

La seconda descrizione è relativa a una struttura in grado di ridimensionare le stringhe.

 

 