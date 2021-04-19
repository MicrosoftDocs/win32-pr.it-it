---
description: Il \_ metodo Get MediaType restituisce il tipo di supporto di output corrente del filtro Resizer.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Metodo IResize:: get_MediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332569"
---
# <a name="iresizeget_mediatype-method"></a>Metodo IResize:: Get \_ mediaType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `get_MediaType` metodo restituisce il tipo di supporto di output corrente del filtro Resizer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* \[ out\]
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata dal chiamante. Il metodo compila questa struttura con il tipo di supporto. Il chiamante deve rilasciare il blocco di formato, se disponibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Se il tipo di supporto di output non è stato impostato, restituire un tipo di supporto predefinito. Il filtro deve aggiornare il tipo di supporto di output quando vengono chiamati i metodi **put \_ mediaType** o **put \_ size** . il tipo di supporto restituito da `get_MediaType` deve riflettere queste modifiche.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9,0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IResize**](iresize.md)
</dt> </dl>

 

 




