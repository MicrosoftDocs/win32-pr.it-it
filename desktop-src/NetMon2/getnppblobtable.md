---
description: La funzione GetNPPBlobTable recupera una tabella BLOB NPP che rappresenta le schede di interfaccia di rete del registro nel computer locale.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Funzione GetNPPBlobTable (Netmon.h)
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
ms.openlocfilehash: 49920df1be929eb9b35781aeabdcdf47167e82a94066e2d3237207dd00b08f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910701"
---
# <a name="getnppblobtable-function"></a>Funzione GetNPPBlobTable

La **funzione GetNPPBlobTable** recupera una tabella BLOB NPP che rappresenta le schede di interfaccia di rete del registro nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFilterBlob* \[ Pollici\]
</dt> <dd>

Handle a un BLOB di filtro che limita i BLOB NPP restituiti nella tabella.

</dd> <dt>

*ppBlobTable* \[ Cambio\]
</dt> <dd>

Puntatore a [una struttura BLOB \_ TABLE](blob-table.md) che contiene almeno un puntatore BLOB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                | Descrizione                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ NPP \_ DLL**</dt> </dl>         | Non sono state trovate DLL nella directory NPP.<br/>                    |
| <dl> <dt>**NMERR \_ NO \_ VALID \_ NPP DLLS (NESSUNA DLL NPP \_ VALIDA)**</dt> </dl> | Nessuna DLL nella directory NPP era valida.<br/>  |
| <dl> <dt>**NMERR \_ NO \_ MATCHING \_ NPPS**</dt> </dl>   | Sono stati individuati BLOB NPP, ma nessuno ha superato il test del filtro.<br/> |
| <dl> <dt>**NMERR \_ OUT \_ OF \_ MEMOR**</dt> </dl>       | Network Monitor non è stato in grado di allocare memoria.<br/>            |



 

## <a name="remarks"></a>Commenti

Anche il BLOB denominato *da hFilterBlob* può essere un BLOB speciale.

Se si imposta il flag nel BLOB del filtro su **TRUE,** la tabella BLOB restituita può includere anche BLOB speciali.

Se il BLOB denominato *da hFilterBlob* è un BLOB speciale, l'Network Monitor'interfaccia utente tenterà di elaborarlo. Si supponga, ad esempio, che una chiamata precedente restituisca un BLOB speciale dal servizio NPP remoto. L'applicazione inserisce il tag richiesto, MACHINE \_ NAME. Il finder passa quindi questo BLOB all'NPP remoto, che quindi restituisce una tabella dei BLOB NPP associati al nome del computer.

Per eliminare tutti i BLOB restituiti e la tabella BLOB, il chiamante è responsabile della chiamata alla **funzione DestroyBlob.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




