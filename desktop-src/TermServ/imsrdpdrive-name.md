---
title: Proprietà Name di IMsRdpDrive
description: Recupera il nome dell'unità.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà nome
- Nome Servizi Desktop remoto proprietà, interfaccia IMsRdpDrive
- Interfaccia IMsRdpDrive Servizi Desktop remoto, proprietà Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477740"
---
# <a name="imsrdpdrivename-property"></a>Proprietà IMsRdpDrive:: Name

Recupera il nome dell'unità.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>Valore proprietà

Nome dell'unità.

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, viene restituito **S \_ OK** . Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.

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

 

 





