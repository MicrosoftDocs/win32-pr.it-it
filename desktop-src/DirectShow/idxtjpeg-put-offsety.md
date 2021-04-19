---
description: Il \_ metodo di offset put specifica l'offset verticale dell'origine della cancellazione.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: 'IDxtJpeg: metodo:p ut_OffsetY (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331918"
---
# <a name="idxtjpegput_offsety-method"></a>IDxtJpeg::p \_ metodo di offset UT

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_OffsetY` metodo specifica l'offset verticale dell'origine della cancellazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Offset verticale dell'origine della cancellazione, espresso in pixel. Il centro della cancellazione viene sottoposta a offset in base a questa quantità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

[**Interfaccia IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




