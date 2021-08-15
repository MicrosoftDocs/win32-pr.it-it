---
title: Metodo IVMTask WaitForCompletion (VPCCOMInterfaces.h)
description: Attende il completamento dell'attività o la scadenza dell'intervallo di timeout specificato.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- Metodo WaitForCompletion Virtual PC
- Metodo WaitForCompletion Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, metodo WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd77019c98e48f4707ac173f825823d5637a1d83c5eb1583f4ee68874e84bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752702"
---
# <a name="ivmtaskwaitforcompletion-method"></a>Metodo IVMTask::WaitForCompletion

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Attende il completamento dell'attività o la scadenza dell'intervallo di timeout specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*timeout* \[ Pollici\]
</dt> <dd>

Tempo di attesa, in millisecondi, del completamento dell'attività da parte di questo metodo prima di restituire il controllo al chiamante. Il valore -1 specifica che il metodo attenderà il completamento dell'attività senza timeout. Altri valori di timeout validi sono da 0 a 4.000.000 millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | Il *parametro timeout* non è valido.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Il **metodo WaitForCompletion** inserisce il thread di esecuzione corrente in stato di sospensione fino a quando non viene restituito. Non è consigliabile specificare un'attesa infinita (timeout = -1) a meno che non sia assolutamente fondamentale che l'attività venga completata in qualsiasi circostanza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attività IVM**](ivmtask.md)
</dt> </dl>

 

