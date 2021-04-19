---
description: 'Il metodo FreeProps libera le risorse allocate dal metodo IPropertySetter:: GetProps. Chiamare questo metodo dopo la chiamata a GetProps, passandogli le strutture restituite da GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Metodo IPropertySetter:: FreeProps (qedit. h)'
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
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325481"
---
# <a name="ipropertysetterfreeprops-method"></a>Metodo IPropertySetter:: FreeProps

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `FreeProps` metodo libera le risorse allocate dal metodo [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) . Chiamare questo metodo dopo la chiamata a **GetProps**, passandogli le strutture restituite da **GetProps**.

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

*cParams* \[ in\]
</dt> <dd>

Numero di elementi nella matrice *Pieri* .

</dd> <dt>

*Pieri* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture di [**\_ parametri Dexter**](dexter-param.md) .

</dd> <dt>

*paValue* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture di [**\_ valori Dexter**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




