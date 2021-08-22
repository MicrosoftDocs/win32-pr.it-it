---
description: Determina se un dispositivo di input supporta multitouch.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: Metodo ITablet3::IsMultiTouch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: bbdd18d27c8b9f5f4b7567e6aa22fd0c74f5e2c2dc74d80e1f46aca4195b93ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717300"
---
# <a name="itablet3ismultitouch-method"></a>Metodo ITablet3::IsMultiTouch

Determina se un dispositivo di input supporta multitouch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIsMultiTouch* \[ Cambio\]
</dt> <dd>

Indica se il dispositivo è multitouch.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo, in caso contrario restituisce un codice di errore, ad esempio E **\_ FAIL**.

## <a name="remarks"></a>Commenti

Dopo aver determinato tramite [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) o **ITablet3::IsMultiTouch** che multitouch è disponibile, un'applicazione può scegliere di acconsentire esplicitamente ai messaggi di input multitouch. Altre informazioni sul filtro dei metodi multitouch sono disponibili nella sezione della proprietà **IRealTimeStylus3::MultiTouchEnabled.**

## <a name="examples"></a>Esempio


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




