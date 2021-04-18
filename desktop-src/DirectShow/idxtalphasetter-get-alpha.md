---
description: Il \_ metodo Get Alpha Recupera il valore alfa per l'intera immagine.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Metodo IDxtAlphaSetter:: get_Alpha (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327922"
---
# <a name="idxtalphasetterget_alpha-method"></a>Metodo IDxtAlphaSetter:: Get \_ Alpha

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_Alpha` metodo recupera il valore alfa per l'intera immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Riceve il valore alfa. Questo valore alfa verrà applicato all'intera immagine di destinazione. Un valore negativo indica che non è impostato alcun valore alfa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                               | Descrizione                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null**<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                   |



 

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

[**Interfaccia IDxtAlphaSetter**](idxtalphasetter.md)
</dt> </dl>

 

 




