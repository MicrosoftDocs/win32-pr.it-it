---
description: La funzione SelectNPPBlobFromTable seleziona una scheda di interfaccia di rete da una tabella BLOB NPP fornita.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Funzione SelectNPPBlobFromTable (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14d9ca14d027efc1540f5a5d2ae78e948da68dd59247252989b617d07229bb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074411"
---
# <a name="selectnppblobfromtable-function"></a>Funzione SelectNPPBlobFromTable

La **funzione SelectNPPBlobFromTable** seleziona una scheda di interfaccia di rete da una tabella BLOB NPP fornita.

## <a name="syntax"></a>Sintassi


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra in cui viene visualizzata **la finestra di dialogo** Seleziona una rete.

</dd> <dt>

*pBlobTable* \[ Pollici\]
</dt> <dd>

Puntatore alla tabella BLOB fornita. Network Monitor questa tabella viene utilizzata per popolare la **finestra di dialogo** Seleziona una rete.

</dd> <dt>

*hBlob* \[ Cambio\]
</dt> <dd>

Handle al BLOB che rappresenta la scheda di interfaccia di rete selezionata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo e l'utente seleziona una scheda di interfaccia di rete, il valore restituito è NMERR SUCCESS. Il BLOB a cui \_ *punta hBlob* viene compilato.

Se l'utente non seleziona una scheda di interfaccia di rete, il valore restituito è NMERR \_ NO \_ NPP \_ SELECTED.

Se la funzione ha esito negativo, il valore restituito è un altro valore NMERR.

## <a name="remarks"></a>Commenti

Quando viene chiamato, Network Monitor viene visualizzata **la finestra** di dialogo Seleziona una rete, che è possibile usare per selezionare una scheda di interfaccia di rete. Il BLOB NPP che rappresenta la scheda di interfaccia di rete selezionata torna all'applicazione chiamante.

Per informazioni sui vari modi in cui è possibile selezionare le schede di interfaccia di rete, vedere [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Voci BLOB speciali](special-blob-entries.md)
</dt> </dl>

 

 




