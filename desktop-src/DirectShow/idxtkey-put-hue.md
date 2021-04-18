---
description: Il \_ metodo Put Hue specifica il valore Hue per il quale eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ Hue.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'IDxtKey: metodo:p ut_Hue (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326913"
---
# <a name="idxtkeyput_hue-method"></a>IDxtKey: metodo:p UT \_ Hue

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_Hue` metodo specifica il valore Hue per il quale eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ Hue.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newVal* \[ in\]
</dt> <dd>

Valore di tonalità su cui eseguire la chiave. L'intervallo valido è compreso tra 0 e 360.

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

[**Interfaccia IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey: tipo di:p di \_ tipo UT**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




