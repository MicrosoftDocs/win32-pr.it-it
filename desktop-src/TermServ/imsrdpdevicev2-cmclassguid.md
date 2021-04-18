---
title: Proprietà CmClassGuid di IMsRdpDeviceV2
description: Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CmClassGuid
- Servizi Desktop remoto proprietà CmClassGuid, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300991"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>Proprietà IMsRdpDeviceV2:: CmClassGuid

Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Valore proprietà

GUID della classe di installazione di Configuration Manager per il dispositivo.

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

 

 





