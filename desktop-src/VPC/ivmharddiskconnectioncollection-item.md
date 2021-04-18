---
title: Proprietà Item di IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Recupera l'oggetto connessione al disco rigido che corrisponde all'indice specificato.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Proprietà elemento Virtual PC
- Proprietà elemento Virtual PC, interfaccia IVMHardDiskConnectionCollection
- Interfaccia IVMHardDiskConnectionCollection Virtual PC, proprietà Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300934"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>Proprietà IVMHardDiskConnectionCollection:: Item

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'oggetto connessione al disco rigido che corrisponde all'indice specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>Valore proprietà

Oggetto [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata. <br/>                                                      |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro *hardDiskConnection* è **null**. <br/>                                    |
| <dl> <dt>Disp \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | L'indice dell'elemento richiesto non corrisponde a un elemento in questa raccolta. <br/> |
| <dl> <dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt> </dl> | La configurazione è sconosciuta.<br/>                                                       |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                               |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

