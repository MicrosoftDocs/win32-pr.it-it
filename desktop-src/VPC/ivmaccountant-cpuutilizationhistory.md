---
title: Proprietà IVMAccountant CPUUtilizationHistory (VPCCOMInterfaces.h)
description: Recupera l'utilizzo recente della CPU di questa macchina virtuale (come matrice di valori percentuali).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- CPUUtilizationHistory - proprietà Virtual PC
- CPUUtilizationHistory proprietà Virtual PC , interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà CPUUtilizationHistory
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81014d1f72fa6bb0266ed113f40044b46ba15673aec97fdf763a81f6f22f94c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007291"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a>Proprietà IVMAccountant::CPUUtilizationHistory

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera l'utilizzo recente della CPU di questa macchina virtuale (come matrice di valori percentuali).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a>Valore proprietà

Uso recente della CPU di questa macchina virtuale. Questi dati vengono restituiti come matrice di 60 elementi che rappresentano la percentuale di utilizzo della CPU al secondo nell'ultimo minuto. Il tipo variant è VT \_ ARRAY \| VT \_ UI1.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                           |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>                                              |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La macchina virtuale non è in esecuzione. Tutti i 60 elementi della matrice sono impostati su 0.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMAccountant è definito come \_ 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

