---
description: Il metodo SetMediaType specifica il tipo di supporto per la connessione sul pin di input di Sample Grabber.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: Metodo ISampleGrabber::SetMediaType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 060ff0cc10fed441fdb2d6f2bf1bd0e66f3e8b9facec3cb52d8f270b350b1f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817702"
---
# <a name="isamplegrabbersetmediatype-method"></a>Metodo ISampleGrabber::SetMediaType

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetMediaType` metodo specifica il tipo di supporto per la connessione sul pin di input di Sample Grabber.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pType* 
</dt> <dd>

Il puntatore a [**una struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) specifica il tipo di supporto richiesto. Non è necessario impostare tutti i membri della struttura. Per informazioni dettagliate, vedere La sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, Sample Grabber non ha un tipo di supporto preferito. Per assicurarsi che Sample Grabber si connetta al filtro corretto, chiamare questo metodo prima di compilare il grafico del filtro.

Questo metodo limita l'intervallo di tipi di supporti che il filtro accetterà. Quando il filtro si connette, tenta di trovare la corrispondenza con il tipo di supporto specificato in *pType*. A tale scopo, confronta i GUID del tipo principale, del sottotipo e del tipo di formato, in questo ordine. Per ognuno di questi GUID, se *pType* ha il valore GUID NULL, Sample Grabber accetta il tipo di supporto \_ senza ulteriori controlli. Se *pType* ha qualsiasi altro valore, Sample Grabber lo confronta con il GUID nel tipo di connessione. A meno che i due GUID non corrispondano esattamente, Sample Grabber rifiuta la connessione.

Per i tipi di file multimediali video, Sample Grabber ignora il blocco di formato. Pertanto, accetterà qualsiasi dimensione video e frequenza dei fotogrammi. Quando si chiama `SetMediaType` , impostare il blocco di formato (**pbFormat**) su **NULL** e le dimensioni (**cbFormat**) su zero. Per i tipi di supporti audio, Sample Grabber esaminerà la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) e richiederà che l'altro filtro si connetta a tale formato, a meno che il blocco di formato in *pType* non sia **NULL** o che il tag di formato sia WAVE FORMAT PCM e gli altri membri della struttura non siano pari a \_ \_ zero.

Esempio 1:

-   Tipo principale: MEDIATYPE \_ Video
-   Sottotipo: GUID \_ NULL
-   Tipo di formato: GUID \_ NULL

Sample Grabber accetterà qualsiasi tipo di video in cui il tipo principale è uguale a MEDIATYPE \_ Video. Non controlla il sottotipo.

Esempio 2:

-   Tipo principale: MEDIATYPE \_ Video
-   Sottotipo: MEDIASUBTYPE \_ RGB24
-   Tipo di formato: GUID \_ NULL

A questo punto, Sample Grabber controlla il sottotipo e accetta solo video RGB 24.

**Limitazioni:** Indipendentemente dal tipo impostato, sample Grabber Filter rifiuta tutti i tipi di video con orientamento dall'alto verso il basso *(biHeight* negativo) o con un tipo di formato FORMAT \_ VideoInfo2. In questo caso, anche se `SetMediaType` il metodo ha esito positivo, il filtro non si connetterà.

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

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 
