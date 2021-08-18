---
title: Proprietà IMsRdpDeviceV2 DriveLetterBitmap
description: Contiene un campo di bit che rappresenta una mappa di lettere di unità contenute nel dispositivo.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Proprietà DriveLetterBitmap Servizi Desktop remoto
- Proprietà DriveLetterBitmap Servizi Desktop remoto, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto , proprietà DriveLetterBitmap
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
ms.openlocfilehash: af03d0e9e77a2a6a9d83e40fc2943bd5365d1312a1ca744aedf3b9331b719f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138594"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a>Proprietà IMsRdpDeviceV2::D riveLetterBitmap

Contiene un campo di bit che rappresenta una mappa di lettere di unità contenute nel dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a>Valore proprietà

Mappa di lettere di unità contenute all'interno del dispositivo. Ogni bit nel valore rappresenta una lettera di unità. Il bit meno significativo rappresenta la lettera di unità "A", il bit successivo rappresenta la lettera di unità "B" e così via.

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

 

 





