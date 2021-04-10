---
description: Il metodo Remove dell'oggetto SWbemPropertySet Elimina una proprietà dalla raccolta SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Metodo SWbemPropertySet. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130979"
---
# <a name="swbempropertysetremove-method"></a>Metodo SWbemPropertySet. Remove

Il metodo **Remove** dell'oggetto [**SWbemPropertySet**](swbempropertyset.md) Elimina una proprietà dalla raccolta **SWbemPropertySet** .

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strName* \[ in\]
</dt> <dd>

Obbligatorio. Nome dell'elemento da rimuovere.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato. Se specificato, questo valore deve essere 0 (zero).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **Remove** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

L'utente ha tentato di eliminare una proprietà che non può essere eliminata.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

La proprietà specificata non esiste.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per l'esecuzione di questo metodo.

</dd> <dt>

**wbemErrPropagatedProperty** -142927303552 (0x2147219380)
</dt> <dd>

L'utente ha tentato di eliminare una proprietà che non possedeva. La proprietà è stata ereditata da una classe padre.

</dd> <dt>

**wbemErrResetToDefault** -2147758082 (0x80043002)
</dt> <dd>

L'utente ha eliminato un valore predefinito di sostituzione per la classe corrente. Il valore predefinito per questa proprietà nella classe padre è stato riattivato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è possibile rimuovere le proprietà dalle istanze della classe o dalle classi derivate con proprietà ereditate. Tali tentativi di eliminazione generano un errore e la proprietà non viene rimossa. la proprietà viene reimpostata sul valore predefinito.

Non è possibile eseguire l'iterazione di una raccolta durante la rimozione degli elementi perché quando si rimuove un elemento da una raccolta, il puntatore alla raccolta viene spostato nell'elemento successivo. Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).

## <a name="examples"></a>Esempio

Per un esempio di codice che usa questo metodo, vedere l'argomento [**SWbemPropertySet**](swbempropertyset.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMPROPERTYSET IID<br/>                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Add**](swbempropertyset-add.md)
</dt> </dl>

 

 




