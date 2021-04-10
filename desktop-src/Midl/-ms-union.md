---
title: /ms_union opzione
description: L' \_ opzione Union/MS controlla l'allineamento del rapporto di recapito delle unioni non incapsulate. Nota Questo attributo viene fornito per la compatibilità con le versioni precedenti.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union switch MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857549"
---
# <a name="ms_union-switch"></a>\_Switch Unione/MS

L' **opzione \_ Union/MS** controlla l'allineamento del rapporto di recapito delle unioni non incapsulate.

> [!Note]  
> Questo attributo viene fornito per la compatibilità con le versioni precedenti. Non è consigliabile usarlo in una nuova interfaccia.

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Il compilatore MIDL riflette il comportamento del compilatore IDL OSF-DCE per le unioni non incapsulate. Tuttavia, poiché le versioni precedenti del compilatore MIDL non lo hanno fatto, l' **opzione \_ Union/MS** fornisce la compatibilità con le interfacce compilate in versioni precedenti del compilatore MIDL.

La \_ funzionalità di MS Union può essere utilizzata come opzione della riga di comando (**/MS \_ Union**), un attributo di interfaccia IDL o come attributo di tipo IDL.

## <a name="examples"></a>Esempio

**\_file. idl di MIDL/MS Union**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




