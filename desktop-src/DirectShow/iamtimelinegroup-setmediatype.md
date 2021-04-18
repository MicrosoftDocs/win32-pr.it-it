---
description: Il metodo SetMediaType imposta il tipo di supporto non compresso per il gruppo.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'Metodo IAMTimelineGroup:: SetMediaType (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331632"
---
# <a name="iamtimelinegroupsetmediatype-method"></a>Metodo IAMTimelineGroup:: SetMediaType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMediaType` metodo imposta il tipo di supporto non compresso per il gruppo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* \[ in\]
</dt> <dd>

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che descrive il formato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                             | Descrizione                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                             |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Argomento puntatore **null** .<br/>           |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Il tipo di supporto specificato non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

Sono supportati i tipi di supporto seguenti:

-   Video RGB non compresso
-   16 bit per pixel, formato 555 (MEDIASUBTYPE \_ RGB555)
-   24 bit per pixel (MEDIASUBTYPE \_ RGB24)
-   32 bit per pixel, con alfa (MEDIASUBTYPE \_ ARGB32, not MEDIASUBTYPE \_ rgb32)
-   audio PCM stereo a 16 bit ( \_ PCM MEDIASUBTYPE)

I tipi di video devono usare il formato \_ videoinfo per il tipo di formato e [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per il blocco di formato. Il formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) non è supportato. Inoltre, i formati video dall'alto verso il basso (*biHeight* < 0) non sono supportati.

Per specificare un formato di compressione per il gruppo, chiamare il metodo [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .

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

[**Interfaccia IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




