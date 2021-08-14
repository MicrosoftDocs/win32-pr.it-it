---
title: IMsRdpDrive RedirectionState - proprietà
description: Indica lo stato di reindirizzamento dell'unità.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Proprietà RedirectionState Servizi Desktop remoto
- Proprietà RedirectionState Servizi Desktop remoto,interfaccia IMsRdpDrive
- Interfaccia IMsRdpDrive Servizi Desktop remoto proprietà RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6069ec911210fac3f4334bdf9e84da080e5536a4f4b6cfc7aca0e54fe0bd2228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351959"
---
# <a name="imsrdpdriveredirectionstate-property"></a>Proprietà IMsRdpDrive::RedirectionState

Indica lo stato di reindirizzamento dell'unità.

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

Impostare questo parametro su **VARIANT \_ FALSE.** per disabilitare il reindirizzamento o **VARIANT \_ TRUE.** per abilitare il reindirizzamento.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, **viene restituito S \_ OK.** Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive è definito come d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





