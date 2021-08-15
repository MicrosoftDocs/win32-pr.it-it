---
description: Il metodo FreeProps libera le risorse allocate dal metodo IPropertySetter::GetProps. Chiamare questo metodo dopo aver chiamato GetProps, passando le strutture restituite da GetProps.
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: Metodo IPropertySetter::FreeProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 34529c7d78ad36a87eb441f624af8daf1167a77148758ff376feacc70250f18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397552"
---
# <a name="ipropertysetterfreeprops-method"></a>Metodo IPropertySetter::FreeProps

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `FreeProps` metodo libera le risorse allocate dal metodo [**IPropertySetter::GetProps.**](ipropertysetter-getprops.md) Chiamare questo metodo dopo aver **chiamato GetProps**, passando le strutture restituite da **GetProps**.

## <a name="syntax"></a>Sintassi


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cParams* \[ Pollici\]
</dt> <dd>

Numero di elementi nella matrice *paParam.*

</dd> <dt>

*paParam* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di [**strutture PARAM DI TIPO \_ PARAM.**](dexter-param.md)

</dd> <dt>

*paValue* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di [**strutture DEXTER \_**](dexter-value.md) VALUE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




