---
title: Metodo IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Attende il completamento dell'attività o l'intervallo di timeout specificato.
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
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302098"
---
# <a name="ivmtaskwaitforcompletion-method"></a>Metodo IVMTask:: WaitForCompletion

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attende il completamento dell'attività o l'intervallo di timeout specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*timeout* \[ in\]
</dt> <dd>

Tempo, in millisecondi, durante il quale questo metodo attenderà il completamento dell'attività prima di restituire il controllo al chiamante. Il valore-1 indica che il metodo resterà in attesa fino al completamento dell'attività senza timeout. Altri valori di timeout validi sono compresi tra 0 e 4 milioni millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>         |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>      | Il parametro *timeout* non è valido.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>     |



 

## <a name="remarks"></a>Commenti

Il metodo **WaitForCompletion** inserisce il thread di esecuzione corrente in modalità di sospensione fino a quando non viene restituito. Non è consigliabile specificare un'attesa infinita (timeout =-1), a meno che non sia assolutamente fondamentale che l'attività venga completata in qualsiasi circostanza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

