---
title: Proprietà DriveLetterBitmap di IMsRdpDeviceV2
description: Contiene un bit che rappresenta una mappa delle lettere di unità contenute all'interno del dispositivo.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DriveLetterBitmap
- Servizi Desktop remoto proprietà DriveLetterBitmap, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà DriveLetterBitmap
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739994"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a>IMsRdpDeviceV2::D Proprietà riveLetterBitmap

Contiene un bit che rappresenta una mappa delle lettere di unità contenute all'interno del dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a>Valore proprietà

Mappa delle lettere di unità contenute all'interno del dispositivo. Ogni bit nel valore rappresenta una lettera di unità. Il bit meno significativo rappresenta la lettera di unità "A", il bit successivo rappresenta la lettera di unità "B" e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 con SP1<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2 con SP1<br/>                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





