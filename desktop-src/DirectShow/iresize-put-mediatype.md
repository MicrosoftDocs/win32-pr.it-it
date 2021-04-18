---
description: Il \_ metodo Put MediaType imposta il tipo di supporto di output sul filtro Resizer.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize: metodo:p ut_MediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327327"
---
# <a name="iresizeput_mediatype-method"></a>IResize::p UT \_ mediaType metodo

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `put_MediaType` metodo imposta il tipo di supporto di output sul filtro Resizer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* \[ in\]
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

DES chiama questo metodo prima di connettere il pin di output del filtro. Usare il tipo di supporto come tipo di supporto del PIN di output. Restituire questo tipo di supporto nel metodo [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) e selezionare contro questo tipo nel metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) . DES non chiama mai questo metodo dopo la connessione del PIN di output.

Attualmente, DES imposta sempre il tipo di supporto di output su un formato RGB non compresso con un blocco di formato **VIDEOINFOHEADER** (il tipo di formato è uguale a Format \_ videoinfo). Il sottotipo potrebbe essere MEDIASUBTYPE \_ ARGB32, che indica RGB a 32 bit con un canale alfa.

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

 

 




