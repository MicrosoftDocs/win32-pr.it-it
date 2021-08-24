---
title: Opzione /ms_union
description: L'opzione /ms union controlla l'allineamento del rapporto di mancato recapito delle \_ unioni non incapsulate. Nota Questo attributo viene fornito per la compatibilità con le versioni precedenti.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union l'opzione MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b8e2f4b86929954ad67c845cf546d46f5950698fce7c21d721613af3611a066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811391"
---
# <a name="ms_union-switch"></a>Opzione /ms \_ union

**L'opzione /ms \_ union** controlla l'allineamento NDR delle unioni non incapsulate.

> [!Note]  
> Questo attributo viene fornito per la compatibilità con le versioni precedenti. Non è consigliabile usarla in una nuova interfaccia.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Il compilatore MIDL rispecchia il comportamento del compilatore IDL OSF-DCE per le unioni non incapsulate. Tuttavia, poiché le versioni precedenti del compilatore MIDL non lo hanno fatto, l'opzione **/ms \_ union** garantisce la compatibilità con le interfacce compilate nelle versioni precedenti del compilatore MIDL.

La funzionalità ms union può essere usata come opzione della riga di comando ( /ms union ), come attributo di interfaccia IDL o \_ come attributo di tipo IDL.**\_**

## <a name="examples"></a>Esempio

**midl /ms \_ union file.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




