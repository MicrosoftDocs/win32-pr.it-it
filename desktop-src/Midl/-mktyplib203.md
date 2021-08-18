---
title: Opzione /mktyplib203
description: L'opzione /mktyplib203 forza il compilatore MIDL ad analizzare il file di input.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- Opzione /mktyplib203 MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc887560401986b9a7d5e0f0aa7c8b36d61874bf245a88ade7a149cd084f1ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014149"
---
# <a name="mktyplib203-switch"></a>Opzione /mktyplib203

**L'opzione /mktyplib203 forza** il compilatore MIDL ad analizzare il file di input.

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Per usare l'opzione **/mktyplib203,** il file di input deve seguire esattamente la sintassi ODL, ovvero non è possibile inserire istruzioni all'esterno del blocco di libreria. Esempio

**midl /mktyplib203 myoldodl.odl**

**midl /mktyplib203 oldhabit.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




