---
description: Dichiara un nuovo indice nel database specificato.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Funzione SdbDeclareIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: b428699641d5a18bad8a1869f59ab1bb5402e7b667526070c3dc0575e435fc38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666590"
---
# <a name="sdbdeclareindex-function"></a>Funzione SdbDeclareIndex

Dichiara un nuovo indice nel database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tWhich* \[ Pollici\]
</dt> <dd>

Questo parametro deve essere **TAG \_ TYPE \_ LIST.**

</dd> <dt>

*tKey* \[ Pollici\]
</dt> <dd>

TAG che specifica il tipo da usare come chiave. Questo parametro non può essere **TAG \_ TYPE \_ LIST**.

</dd> <dt>

*dwEntries* \[ Pollici\]
</dt> <dd>

Numero di voci da allocare nell'indice.

</dd> <dt>

*bUniqueKey* \[ Pollici\]
</dt> <dd>

Se questo parametro è **TRUE,** l'indice è un indice di chiave univoca.

</dd> <dt>

*piiIndex* \[ Cambio\]
</dt> <dd>

INDEXID **risultante** dell'indice appena dichiarato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di errore.

## <a name="remarks"></a>Commenti

Chiamare questa funzione prima di scrivere tag nel nuovo indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INDEXID**](indexid.md)
</dt> <dt>

[**SdbCommitIndexes**](sdbcommitindexes.md)
</dt> <dt>

[**SdbStartIndexing**](sdbstartindexing.md)
</dt> <dt>

[**SdbStopIndexing**](sdbstopindexing.md)
</dt> </dl>

 

 




