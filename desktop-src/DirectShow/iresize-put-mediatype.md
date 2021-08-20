---
description: Il metodo put \_ MediaType imposta il tipo di supporto di output sul filtro di ridimensionamento.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: Metodo IResize::p ut_MediaType (Qedit.h)
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
ms.openlocfilehash: 6c26878af6f091efd3c3f321cb073ce51a8e6236d4bafa326ab99f85f39e1a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818202"
---
# <a name="iresizeput_mediatype-method"></a>Metodo IResize::p ut \_ MediaType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `put_MediaType` metodo imposta il tipo di supporto di output sul filtro di ridimensionamento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pmt* \[ Pollici\]
</dt> <dd>

Puntatore a una [**\_ struttura AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

DES chiama questo metodo prima di connettere il pin di output del filtro. Usare il tipo di supporto come tipo di supporto del pin di output. Restituisce questo tipo di supporto nel metodo [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) e controlla agsint questo tipo nel metodo [**CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md) DES non chiama mai questo metodo dopo la connessione del pin di output.

Attualmente DES imposta sempre il tipo di supporto di output su un formato RGB non compresso con un blocco di formato **VIDEOINFOHEADER** (il tipo di formato è uguale a FORMAT \_ VideoInfo). Il sottotipo potrebbe essere MEDIASUBTYPE ARGB32, che indica RGB a \_ 32 bit con un canale alfa.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9.0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IResize**](iresize.md)
</dt> </dl>

 

 




