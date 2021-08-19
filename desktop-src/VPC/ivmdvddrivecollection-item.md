---
title: Proprietà IVMDVDDriveCollection Item (VPCCOMInterfaces.h)
description: Recupera l'oggetto unità CD o DVD corrispondente all'indice specificato.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Proprietà Item Virtual PC
- Proprietà Item Virtual PC, interfaccia IVMDVDDriveCollection
- Interfaccia IVMDVDDriveCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ea8cd86d45827c06f4ef3582cc0d2ff990a176e244483db52101deb596745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753742"
---
# <a name="ivmdvddrivecollectionitem-property"></a>Proprietà IVMDVDDriveCollection::Item

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera l'oggetto unità CD o DVD corrispondente all'indice specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IVMDVDDrive.**](ivmdvddrive.md)

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata. <br/>                                                      |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>                                                          |
| <dl> <dt>E \_ FAIL</dt> <dt>0x80004005</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta. <br/> |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl> | La configurazione è sconosciuta.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection è definito come bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

