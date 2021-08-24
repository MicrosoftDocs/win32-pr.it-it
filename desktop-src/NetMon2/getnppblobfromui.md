---
description: Seleziona una scheda di interfaccia di rete del registro.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Funzione GetNPPBlobFromUI (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d3b88c369145d53d32d23773072f878d9834110e705cd8ff623a3726cbb98b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743881"
---
# <a name="getnppblobfromui-function"></a>Funzione GetNPPBlobFromUI

La **funzione GetNPPBlobFromUI** seleziona una scheda di interfaccia di rete del registro.

## <a name="syntax"></a>Sintassi


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Handle per una finestra che visualizza la **finestra di dialogo** Seleziona una rete.

</dd> <dt>

*hFilterBlob* \[ Pollici\]
</dt> <dd>

Handle di un [*BLOB di*](f.md) filtro usato per limitare le schede di interfaccia di rete visualizzate.

</dd> <dt>

*phBlob* \[ Cambio\]
</dt> <dd>

Puntatore all'handle del BLOB che rappresenta la scheda di interfaccia di rete selezionata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (l'utente seleziona una scheda di interfaccia di rete), il valore restituito è NMERR SUCCESS e il BLOB a cui \_ *punta phBlob* viene compilato.

Se l'utente non seleziona una scheda di interfaccia di rete, il valore restituito **è NMERR \_ NO \_ NPP \_ SELECTED**.

Se la funzione ha esito negativo, il valore restituito è un altro valore NMERR.

## <a name="remarks"></a>Commenti

Quando viene chiamato, Network Monitor viene visualizzata **la finestra** di dialogo Seleziona una rete, che è possibile usare per selezionare una scheda di interfaccia di rete. Il BLOB NPP che rappresenta la scheda di interfaccia di rete viene restituito all'applicazione chiamante.

Se il BLOB denominato *da hFilterBlob* è un [*BLOB*](s.md)speciale, il finder tenterà di elaborarlo. Un esempio è una chiamata che in precedenza aveva restituito un BLOB speciale dal servizio NPP remoto. L'applicazione ha inserito il tag richiesto, MACHINE \_ NAME. In questo caso, il finder passerebbe questo BLOB all'NPP remoto, che restituirebbe quindi una tabella di BLOB NPP che rappresentano il computer richiesto. Questi BLOB NPP remoti verranno visualizzati nella finestra di dialogo.

Il chiamante deve chiamare [la funzione DestroyBlob,](destroyblob.md) che elimina il BLOB restituito quando non è più necessario.



| Per altre informazioni su | Vedere                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Tre modi per selezionare le schede di interfaccia di rete  | [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md) |
| Specifica di un BLOB di filtro   | [Specifica di un BLOB di filtro](specifying-a-filter-blob.md)                     |



 

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

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




