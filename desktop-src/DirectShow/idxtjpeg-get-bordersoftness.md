---
description: Il \_ metodo Get BorderSoftness recupera la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.
ms.assetid: f5648cce-e44c-4ed6-8254-6511cd600629
title: 'Metodo IDxtJpeg:: get_BorderSoftness (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 968dbef4a87a7b88e16321693350d35d08225c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326274"
---
# <a name="idxtjpegget_bordersoftness-method"></a>Metodo IDxtJpeg:: Get \_ BorderSoftness

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_BorderSoftness` metodo recupera la larghezza dell'area sfocata intorno ai bordi del pattern di cancellazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BorderSoftness(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Riceve la larghezza, in pixel, dell'area sfocata.

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

 

 




