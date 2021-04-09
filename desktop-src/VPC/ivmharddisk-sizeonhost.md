---
title: Proprietà IVMHardDisk SizeOnHost (VPCCOMInterfaces. h)
description: Dimensioni del file del disco rigido virtuale nel computer host.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Proprietà SizeOnHost Virtual PC
- Proprietà SizeOnHost Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048575"
---
# <a name="ivmharddisksizeonhost-property"></a>Proprietà IVMHardDisk:: SizeOnHost

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera le dimensioni del file del disco rigido virtuale nel computer host.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valore proprietà

Dimensione, in byte, del file di immagine del disco rigido. Questo valore è una **variante** di tipo **\_ decimale VT**.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                               | Significato                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>           |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro è **null**.<br/>              |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>       |
| <dl> <dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt> </dl> | Il file di immagine del disco rigido non è stato trovato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

