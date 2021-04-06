---
title: Proprietà IVMMouse ScrollWheelPosition (VPCCOMInterfaces. h)
description: Regola la coordinata z del mouse (solo relativa).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Proprietà ScrollWheelPosition Virtual PC
- Proprietà ScrollWheelPosition Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743455"
---
# <a name="ivmmousescrollwheelposition-property"></a>Proprietà IVMMouse:: ScrollWheelPosition

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Regola la coordinata z del mouse (solo relativa).

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Valore proprietà

Coordinata z che indica il numero di pixel che il mouse deve spostare lungo l'asse z.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                     | Significato                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                        | L'operazione è stata completata.<br/>                                                                |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>             | La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.<br/>         |
| <dl> <dt>Macchina virtuale \_ E \_ mouse \_ non \_ attivo</dt> <dt>0xA0040800</dt> </dl>           | Il dispositivo mouse non è stato alimentato o non è attualmente attivo nella macchina virtuale.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ utilizzo \_ delle \_ coordinate assolute</dt> <dt>0xA0040801</dt> </dl> | Impossibile impostare la posizione della rotellina di scorrimento quando il dispositivo mouse utilizza coordinate assolute.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                  | Si è verificato un errore imprevisto.<br/>                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

