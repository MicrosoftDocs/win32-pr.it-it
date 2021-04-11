---
description: Determina se un dispositivo di input supporta il multitouch.
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: 'Metodo ITablet3:: datamultitouch'
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
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233174"
---
# <a name="itablet3ismultitouch-method"></a>Metodo ITablet3:: datamultitouch

Determina se un dispositivo di input supporta il multitouch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bIsMultiTouch* \[ out\]
</dt> <dd>

Indica se il dispositivo è multitouch.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** in caso di esito positivo; in caso contrario, restituisce un codice di errore, ad esempio **E \_ Fail**.

## <a name="remarks"></a>Commenti

Dopo aver determinato l'utilizzo di [**IRealTimeStylus3:: MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) o **ITablet3::** multitouch, il multitouch è disponibile, un'applicazione può scegliere di acconsentire esplicitamente ai messaggi di input multitouch. Altre informazioni sul filtro dei metodi multitouch sono disponibili nella sezione proprietà **IRealTimeStylus3:: MultiTouchEnabled** .

## <a name="examples"></a>Esempio


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> <dt>

[**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




