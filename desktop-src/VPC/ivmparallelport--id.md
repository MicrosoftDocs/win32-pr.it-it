---
title: Metodo _ID IVMParallelPort (VPCCOMInterfaces.h)
description: Recupera l'identificatore interno della porta parallela.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID virtual PC
- _ID virtual PC, interfaccia IVMParallelPort
- Interfaccia IVMParallelPort Virtual PC , _ID metodo
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0c7b3eab7de47d182c94aa9b5fb35aef04e98495ef3e7b39d4547967f3438b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593219"
---
# <a name="ivmparallelport_id-method"></a>Metodo IVMParallelPort:: \_ ID

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera l'identificatore interno della porta parallela.

## <a name="syntax"></a>Sintassi


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*portID* \[ Cambio\]
</dt> <dd>

Identificatore di porta parallela.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                            |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>                               |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                        |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl> | La configurazione per questa macchina virtuale non è valida.<br/> |



 

## <a name="remarks"></a>Commenti

Questa proprietà non può essere utilizzata dai linguaggi di scripting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort è definito come 097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

