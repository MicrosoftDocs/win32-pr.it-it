---
description: La funzione GetNPPBlobTable recupera una tabella BLOB NPP che rappresenta le schede di rete di registrazione nel computer locale.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Funzione GetNPPBlobTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882910"
---
# <a name="getnppblobtable-function"></a>GetNPPBlobTable (funzione)

La funzione **GetNPPBlobTable** recupera una tabella BLOB NPP che rappresenta le schede di rete di registrazione nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFilterBlob* \[ in\]
</dt> <dd>

Handle per un BLOB di filtro che limita i BLOB di NPP restituiti nella tabella.

</dd> <dt>

*ppBlobTable* \[ out\]
</dt> <dd>

Puntatore a una struttura di [ \_ tabella BLOB](blob-table.md) che contiene almeno un puntatore del BLOB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                | Descrizione                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ Nessuna \_ \_ dll NPP**</dt> </dl>         | Non sono state trovate dll nella directory NPP.<br/>                    |
| <dl> <dt>**NMERR \_ Nessuna \_ \_ dll NPP \_ valida**</dt> </dl> | Nessuna dll nella directory NPP era una dll NPP valida.<br/>  |
| <dl> <dt>**NMERR \_ senza \_ \_ centrali corrispondente**</dt> </dl>   | I BLOB di NPP sono stati individuati, ma nessuno ha superato il test di filtro.<br/> |
| <dl> <dt>**NMERR \_ da \_ \_ memor**</dt> </dl>       | Network Monitor non è stato in grado di allocare memoria.<br/>            |



 

## <a name="remarks"></a>Commenti

Il BLOB denominato da *hFilterBlob* può anche essere un BLOB speciale.

Se si imposta il flag nel BLOB di filtro su **true**, la tabella BLOB restituita può includere anche BLOB speciali.

Se il BLOB denominato da *hFilterBlob* è un BLOB speciale, l'interfaccia utente Network Monitor tenterà di elaborarla. Si supponga, ad esempio, che una chiamata precedente restituisca un BLOB speciale dall'oggetto NPP remoto. L'applicazione inserisce il tag necessario, il \_ nome del computer. Il Finder passa quindi questo BLOB all'elemento NPP remoto, che quindi restituisce una tabella dei BLOB di NPP associati al nome del computer.

Per eliminare definitivamente tutti i BLOB restituiti e la tabella BLOB, il chiamante è responsabile della chiamata della funzione **DestroyBlob** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




