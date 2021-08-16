---
description: Il metodo AddProp aggiunge una proprietà al setter di proprietà, con una matrice di coppie tempo-valore che definiscono il valore della proprietà in un intervallo di tempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: Metodo IPropertySetter::AddProp (Qedit.h)
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
ms.openlocfilehash: b2a4cf2f730d177b4eb9323e882d5030c6fc1d658ede574e74d9d222e81d677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818610"
---
# <a name="ipropertysetteraddprop-method"></a>Metodo IPropertySetter::AddProp

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il metodo aggiunge una proprietà al setter di proprietà, con una matrice di coppie tempo-valore che definiscono il valore della `AddProp` proprietà in un intervallo di tempo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Parametro* \[ Pollici\]
</dt> <dd>

[**ESEREA \_ Struttura PARAM**](dexter-param.md) che specifica la proprietà. Il **membro nValues** della struttura deve essere uguale alla dimensione della matrice specificata nel *parametro paValue.*

</dd> <dt>

*paValue* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di [**strutture DI \_ TIPO VALUE**](dexter-value.md) contenenti coppie tempo-valore. La matrice deve essere in ordine temporale crescente. I tempi sono relativi all'ora di inizio dell'effetto o della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

La prima [**struttura DI \_ TIPO VALUE**](dexter-value.md) deve specificare un'ora di riferimento pari a zero e un flag di interpolazione (**dwInterp**) di **JUMP PER ILF \_ JUMP** oppure il metodo restituisce un errore.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




