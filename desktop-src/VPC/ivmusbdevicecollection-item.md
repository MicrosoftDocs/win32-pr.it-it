---
title: Proprietà Item di IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto dispositivo USB che corrisponde all'indice specificato.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMUSBDeviceCollection
- Interfaccia IVMUSBDeviceCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477045"
---
# <a name="ivmusbdevicecollectionitem-property"></a>Proprietà IVMUSBDeviceCollection:: Item

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'oggetto dispositivo USB che corrisponde all'indice specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IVMUSBDevice**](ivmusbdevice.md) .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata. <br/>                                                      |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro *usbDevice* è **null**. <br/>                                             |
| <dl> <dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta. <br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection è definito come 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)
</dt> </dl>

 

