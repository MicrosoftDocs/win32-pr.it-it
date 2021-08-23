---
title: Proprietà IVMVirtualMachine ChassisAssetTag (VPCCOMInterfaces.h)
description: Tag asset dello chassis.
ms.assetid: 469816a8-3078-4960-a5e1-79d65b5fc8fc
keywords:
- Proprietà ChassisAssetTag Virtual PC
- Proprietà ChassisAssetTag Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà ChassisAssetTag
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisAssetTag
- IVMVirtualMachine.get_ChassisAssetTag
- IVMVirtualMachine.put_ChassisAssetTag
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7357546d330f21b55a24babaaad532aca3baca121c221c9f1be6493a6a78fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998691"
---
# <a name="ivmvirtualmachinechassisassettag-property"></a>Proprietà IVMVirtualMachine::ChassisAssetTag

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta il tag dell'asset dello chassis.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ChassisAssetTag(
  [in]          BSTR chassisAssetTag
);

HRESULT get_ChassisAssetTag(
  [out, retval] BSTR *chassisAssetTag
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il tag dell'asset dello chassis.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                               | Significato                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                                               |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                    | Il parametro è **NULL.**<br/>                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | Il parametro è maggiore di 32 caratteri, una stringa vuota o non è valido.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>            | La configurazione è sconosciuta.<br/>                                               |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B</dt> <dt></dt> </dl> | Lo stato della macchina virtuale è in esecuzione o salvato.<br/>                         |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                           |



## <a name="remarks"></a>Commenti

Questa proprietà conterrà informazioni valide solo dopo l'avvio della macchina virtuale per la prima volta. Se viene letta prima dell'avvio iniziale, verrà restituita una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

