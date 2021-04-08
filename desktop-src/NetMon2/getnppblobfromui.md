---
description: Seleziona una scheda di interfaccia di rete Register.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Funzione GetNPPBlobFromUI (Netmon. h)
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
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967775"
---
# <a name="getnppblobfromui-function"></a>GetNPPBlobFromUI (funzione)

La funzione **GetNPPBlobFromUI** seleziona una scheda di interfaccia di rete Register.

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

*HWND* \[ in\]
</dt> <dd>

Handle per una finestra che visualizza la finestra di dialogo **Seleziona rete** .

</dd> <dt>

*hFilterBlob* \[ in\]
</dt> <dd>

Handle per un [*BLOB di filtro*](f.md) usato per limitare le schede di rete visualizzate.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Puntatore all'handle del BLOB che rappresenta la scheda di interfaccia di rete selezionata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (l'utente seleziona una scheda di interfaccia di rete), il valore restituito è NMERR \_ Success e il BLOB a cui punta *phBlob* viene compilato.

Se l'utente non seleziona una scheda di interfaccia di rete, il valore restituito è **NMERR non è stato \_ \_ \_ selezionato alcun NPP**.

Se la funzione ha esito negativo, il valore restituito è un altro valore NMERR.

## <a name="remarks"></a>Commenti

Quando viene chiamato, Network Monitor Visualizza la finestra di dialogo **Seleziona rete** che può essere usata per selezionare una scheda di interfaccia di rete. Il BLOB di NPP che rappresenta la scheda di interfaccia di rete viene restituito all'applicazione chiamante.

Se il BLOB denominato da *hFilterBlob* è un [*BLOB speciale*](s.md), il Finder tenterà di elaborarlo. Un esempio potrebbe essere una chiamata che in precedenza aveva restituito un BLOB speciale dall'oggetto NPP remoto. L'applicazione ha inserito il tag richiesto, il nome del computer \_ . In questa situazione, il Finder passa questo BLOB all'oggetto NPP remoto, che restituisce quindi una tabella di BLOB NPP che rappresenta il computer richiesto. Questi BLOB di NPP remoti verranno visualizzati nella finestra di dialogo.

Il chiamante deve chiamare la funzione [DestroyBlob](destroyblob.md) , che elimina il BLOB restituito quando non è più necessario.



| Per altre informazioni su | Vedere                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| Tre modi per selezionare le schede di rete  | [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md) |
| Specifica di un BLOB di filtro   | [Specifica di un BLOB di filtro](specifying-a-filter-blob.md)                     |



 

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

[GetNPPBlobTable](getnppblobtable.md)
</dt> <dt>

[SelectNPPBlobFromTable](selectnppblobfromtable.md)
</dt> </dl>

 

 




