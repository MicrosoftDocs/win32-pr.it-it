---
description: Dichiara un nuovo indice nel database specificato.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex (funzione)
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
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305071"
---
# <a name="sdbdeclareindex-function"></a>SdbDeclareIndex (funzione)

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

*PDB* \[ in\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tWhich* \[ in\]
</dt> <dd>

Questo parametro deve essere **un \_ \_ elenco di tipi di tag**.

</dd> <dt>

*tKey* \[ in\]
</dt> <dd>

TAG che specifica il tipo da utilizzare come chiave. Questo parametro non può essere un **\_ \_ elenco di tipi di tag**.

</dd> <dt>

*dwEntries* \[ in\]
</dt> <dd>

Numero di voci da allocare nell'indice.

</dd> <dt>

*bUniqueKey* \[ in\]
</dt> <dd>

Se questo parametro è **true**, l'indice è un indice di chiave univoca.

</dd> <dt>

*piiIndex* \[ out\]
</dt> <dd>

**INDEXID** risultante dell'indice appena dichiarato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="remarks"></a>Commenti

Chiamare questa funzione prima di scrivere tag nel nuovo indice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
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

 

 




