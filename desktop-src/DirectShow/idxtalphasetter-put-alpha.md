---
description: Il \_ metodo Put Alpha specifica il valore alfa per l'intera immagine.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter: metodo:p ut_Alpha (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329755"
---
# <a name="idxtalphasetterput_alpha-method"></a>IDxtAlphaSetter: metodo:p UT \_ Alpha

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_Alpha` metodo specifica il valore alfa per l'intera immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Alfa* \[ in\]
</dt> <dd>

Valore alfa. Questo valore verrà applicato all'intera immagine di destinazione. Per disabilitare questa proprietà, impostare un valore negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se si imposta questa proprietà su un valore non negativo, è necessario disabilitare anche la proprietà Alpha ramp, chiamando **put \_ AlphaRamp** con un valore negativo. In caso contrario, non viene eseguito il rendering corretto dell'effetto.

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

[**Interfaccia IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::p UT \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




