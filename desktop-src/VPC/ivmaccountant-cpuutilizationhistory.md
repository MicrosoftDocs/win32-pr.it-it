---
title: Proprietà IVMAccountant CPUUtilizationHistory (VPCCOMInterfaces. h)
description: Recupera l'utilizzo di CPU recente della macchina virtuale, come una matrice di valori percentuali.
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Proprietà CPUUtilizationHistory Virtual PC
- Proprietà CPUUtilizationHistory Virtual PC, interfaccia IVMAccountant
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
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479019"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a>Proprietà IVMAccountant:: CPUUtilizationHistory

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'utilizzo di CPU recente della macchina virtuale, come una matrice di valori percentuali.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a>Valore proprietà

Uso della CPU recente della macchina virtuale. Questi dati vengono restituiti come una matrice di 60 elementi che rappresentano la percentuale di utilizzo della CPU in ogni secondo nel minuto precedente. Il tipo Variant è VT \_ array \| VT \_ Ui1.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                           |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>                                              |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La macchina virtuale non è in esecuzione. Tutti gli elementi della matrice 60 vengono impostati su 0.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant è definito come 6376c067-7f57-4D63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

