---
title: Proprietà IMsRdpDevice FriendlyName
description: Recupera il nome visualizzato per il dispositivo.
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà FriendlyName
- Servizi Desktop remoto proprietà FriendlyName, interfaccia IMsRdpDevice
- Interfaccia IMsRdpDevice Servizi Desktop remoto, proprietà FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740543"
---
# <a name="imsrdpdevicefriendlyname-property"></a>Proprietà IMsRdpDevice:: FriendlyName

Recupera il nome visualizzato per il dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a>Valore proprietà

Nome visualizzato.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, viene restituito **S \_ OK** . Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





