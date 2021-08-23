---
title: Proprietà IVMMouse ScrollWheelPosition (VPCCOMInterfaces.h)
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
ms.openlocfilehash: 334190707cd43e63ce2244f410180b11bf6eb5018ff1482f073903adfb4b7878
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510651"
---
# <a name="ivmmousescrollwheelposition-property"></a>Proprietà IVMMouse::ScrollWheelPosition

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Regola la coordinata z del mouse (solo relativa).

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Valore proprietà

Coordinata z che indica il numero di pixel di spostamento del mouse lungo l'asse z.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                     | Significato                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                        | L'operazione è stata completata.<br/>                                                                |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl>             | La macchina virtuale a cui è collegato il dispositivo mouse non è attualmente in esecuzione.<br/>         |
| <dl> <dt>Macchina virtuale \_ E \_ MOUSE \_ NOT \_ ACTIVE</dt> <dt>0xA0040800</dt> </dl>           | Il dispositivo mouse non è stato acceso o non è attualmente attivo nella macchina virtuale.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ USO DELLE COORDINATE \_ \_ ASSOLUTE</dt> <dt>0XA0040801</dt> </dl> | La posizione della rotellina di scorrimento non può essere impostata quando il dispositivo mouse utilizza coordinate assolute.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                  | Si è verificato un errore imprevisto.<br/>                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse è definito come ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

