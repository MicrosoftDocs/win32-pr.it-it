---
title: Enumerazione VMDVDDriveAttachmentType (VPCCOMInterfaces. h)
description: Specifica ciò che viene collegato a un'unità DVD.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- VMDVDDriveAttachmentType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477393"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a>Enumerazione VMDVDDriveAttachmentType

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Specifica ciò che viene collegato a un'unità DVD.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive \_ None**
</dt> <dd>

Nessun elemento collegato.

</dd> <dt>

<span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**immagine di vmDVDDrive \_**
</dt> <dd>

È presente un file di immagine ISO collegato.

</dd> <dt>

<span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**\_HostDrive vmDVDDrive**
</dt> <dd>

È collegata un'unità CD o DVD host.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive:: Attachment**](ivmdvddrive-attachment.md)
</dt> </dl>

 

