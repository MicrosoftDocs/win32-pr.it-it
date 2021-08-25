---
description: Libera le risorse usate dall'interfaccia IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: Metodo IeAxiService::Cleanup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: de0413c39a4abf47a24913f347ceed0158d0b51aa4e1da0b3005cace1326b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908381"
---
# <a name="ieaxiservicecleanup-method"></a>Metodo IeAxiService::Cleanup

Il **metodo Cleanup** libera le risorse usate dall'interfaccia [**IeAxiService.**](ieaxiservice.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop di Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IeAxiService IID è definito come \_ E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

