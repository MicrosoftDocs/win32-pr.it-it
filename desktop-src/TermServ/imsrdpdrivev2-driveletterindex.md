---
title: Proprietà DriveLetterIndex di IMsRdpDriveV2
description: Contiene l'indice della lettera per l'unità.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DriveLetterIndex
- Servizi Desktop remoto proprietà DriveLetterIndex, interfaccia IMsRdpDriveV2
- Interfaccia IMsRdpDriveV2 Servizi Desktop remoto, proprietà DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964974"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2::D Proprietà riveLetterIndex

Contiene l'indice della lettera per l'unità.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Valore proprietà

Indice della lettera per l'unità. 0 = "A", 1 = "B" e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 con SP1<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





