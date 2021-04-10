---
title: opzione/mktyplib203
description: L'opzione/mktyplib203 impone al compilatore MIDL di analizzare il file di input.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 switch MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857550"
---
# <a name="mktyplib203-switch"></a>opzione/mktyplib203

L'opzione **/mktyplib203** impone al compilatore MIDL di analizzare il file di input.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Per usare l'opzione **/mktyplib203** , è necessario che il file di input segua esattamente la sintassi di FAD. non è quindi possibile inserire istruzioni all'esterno del blocco di libreria. Esempio

**MIDL/mktyplib203 myoldodl. FAD**

**MIDL/mktyplib203 oldhabit. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




