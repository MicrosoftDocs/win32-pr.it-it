---
title: Proprietà IMsRdpDevice RedirectionState
description: Indica lo stato di reindirizzamento del dispositivo.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Proprietà RedirectionState Servizi Desktop remoto
- Proprietà RedirectionState Servizi Desktop remoto, interfaccia IMsRdpDevice
- Interfaccia IMsRdpDevice Servizi Desktop remoto proprietà RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8609c682a7a31d293e6e8a9606c8ae445b0487da0d95399fb4e00d779914bfd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606683"
---
# <a name="imsrdpdeviceredirectionstate-property"></a>Proprietà IMsRdpDevice::RedirectionState

Indica lo stato di reindirizzamento del dispositivo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Valore proprietà

Impostare questo parametro su **VARIANT \_ FALSE per** disabilitare il reindirizzamento o SU VARIANT **\_ TRUE** per abilitare il reindirizzamento.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, **viene restituito S \_ OK.** Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice è definito come 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

 





