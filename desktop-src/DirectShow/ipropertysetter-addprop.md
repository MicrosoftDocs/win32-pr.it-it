---
description: Il metodo AddProp aggiunge una proprietà al setter della proprietà, con una matrice di coppie di valori temporali che definiscono il valore della proprietà in un intervallo di tempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Metodo IPropertySetter:: AddProp (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325485"
---
# <a name="ipropertysetteraddprop-method"></a>Metodo IPropertySetter:: AddProp

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `AddProp` metodo aggiunge una proprietà al setter della proprietà, con una matrice di coppie di valori temporali che definiscono il valore della proprietà in un intervallo di tempo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param* \[ in\]
</dt> <dd>

[**Dexter \_ Struttura PARAM**](dexter-param.md) che specifica la proprietà. Il membro **nValori** della struttura deve essere uguale alla dimensione della matrice specificata nel parametro *paValue* .

</dd> <dt>

*paValue* \[ in\]
</dt> <dd>

Puntatore a una matrice di strutture del [**\_ valore Dexter**](dexter-value.md) che contengono coppie di valori temporali. La matrice deve essere in ordine di tempo crescente. Gli orari sono relativi all'ora di inizio dell'effetto o della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

La prima struttura del [**\_ valore Dexter**](dexter-value.md) deve specificare un'ora di riferimento pari a zero e un flag di interpolazione (**dwInterp**) di **DEXTERF \_ Jump** oppure il metodo restituisce un errore.

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

 

 




