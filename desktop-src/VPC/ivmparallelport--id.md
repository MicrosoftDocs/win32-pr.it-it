---
title: Metodo _ID IVMParallelPort (VPCCOMInterfaces. h)
description: Recupera l'identificatore interno della porta parallela.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- Metodo di _ID Virtual PC
- Metodo _ID Virtual PC, interfaccia IVMParallelPort
- Interfaccia IVMParallelPort Virtual PC, metodo _ID
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
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300926"
---
# <a name="ivmparallelport_id-method"></a>Metodo IVMParallelPort:: \_ ID

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'identificatore interno della porta parallela.

## <a name="syntax"></a>Sintassi


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID porta* \[ out\]
</dt> <dd>

Identificatore della porta parallela.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                            |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>                               |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                        |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl> | La configurazione per questa macchina virtuale non è valida.<br/> |



 

## <a name="remarks"></a>Commenti

Questa proprietà non è utilizzabile dai linguaggi di scripting.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort è definito come 097beecb-0A02-474F-abd6-298b22293fc6<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

