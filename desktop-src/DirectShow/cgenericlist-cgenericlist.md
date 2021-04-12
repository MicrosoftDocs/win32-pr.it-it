---
description: Informazioni sul metodo del costruttore per CGenericList. CGenericList (Wxlist. h). Questo metodo usa i parametri ' pName ' è iItems '.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Costruttore CGenericList. CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356199"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a>Costruttore CGenericList. CGenericList (Wxlist. h)-pName, parametri iItems

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pName* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> <dt>

*iItems* 
</dt> <dd>

Dimensioni della cache del nodo.

</dd> <dt>

*Blocco* 
</dt> <dd>

Non usato.

</dd> <dt>

*spbalet* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, la `CGenericList` classe mantiene una cache di nodi elenco. Se si conosce approssimativamente il numero di elementi che l'elenco conterrà, usare questa versione del costruttore.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Wxlist. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




