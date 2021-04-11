---
description: La funzione SelectNPPBlobFromTable seleziona una scheda di interfaccia di rete da una tabella BLOB NPP specificata.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Funzione SelectNPPBlobFromTable (Netmon. h)
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
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226252"
---
# <a name="selectnppblobfromtable-function"></a>SelectNPPBlobFromTable (funzione)

La funzione **SelectNPPBlobFromTable** seleziona una scheda di interfaccia di rete da una tabella BLOB NPP specificata.

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

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra che visualizza la finestra di dialogo **Seleziona rete** .

</dd> <dt>

*pBlobTable* \[ in\]
</dt> <dd>

Puntatore alla tabella BLOB fornita. Network Monitor usa questa tabella per popolare la finestra di dialogo **Seleziona una rete** .

</dd> <dt>

*hBlob* \[ out\]
</dt> <dd>

Handle per il BLOB che rappresenta la scheda di interfaccia di rete selezionata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo e l'utente seleziona una scheda di interfaccia di rete, il valore restituito è NMERR \_ Success; il BLOB a cui punta *hBlob* viene compilato.

Se l'utente non seleziona una scheda di interfaccia di rete, il valore restituito è NMERR non è stato \_ \_ selezionato alcun NPP \_ .

Se la funzione ha esito negativo, il valore restituito è un altro valore NMERR.

## <a name="remarks"></a>Commenti

Quando viene chiamato, Network Monitor Visualizza la finestra di dialogo **Seleziona rete** che può essere usata per selezionare una scheda di interfaccia di rete. Il BLOB di NPP che rappresenta la scheda di interfaccia di rete selezionata torna all'applicazione chiamante.

Per informazioni sui vari modi in cui è possibile selezionare NIC, vedere [selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetNPPBlobFromUI](getnppblobfromui.md)
</dt> <dt>

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[Voci BLOB speciali](special-blob-entries.md)
</dt> </dl>

 

 




