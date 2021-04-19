---
description: Il metodo SetMediaType specifica il tipo di supporto per la connessione sul pin di input del grabber di esempio.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'Metodo ISampleGrabber:: SetMediaType (qedit. h)'
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
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332641"
---
# <a name="isamplegrabbersetmediatype-method"></a>Metodo ISampleGrabber:: SetMediaType

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetMediaType` metodo specifica il tipo di supporto per la connessione sul pin di input del grabber di esempio.

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

Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) specifica il tipo di supporto richiesto. Non è necessario impostare tutti i membri della struttura. per informazioni dettagliate, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il grabber di esempio non ha un tipo di supporto preferito. Per assicurarsi che il grabber di esempio si connetta al filtro corretto, chiamare questo metodo prima di compilare il grafico del filtro.

Questo metodo limita l'intervallo di tipi di supporti che verrà accettato dal filtro. Quando il filtro si connette, tenta di trovare la corrispondenza con il tipo di supporto specificato in *pType*. A tale scopo, vengono confrontati i GUID di tipo principale, sottotipo e tipo di formato, in questo ordine. Per ognuno di questi GUID, se *pType* ha il valore GUID \_ null, il grabber di esempio accetta il tipo di supporto senza ulteriori controlli. Se *pType* ha un altro valore, il grabber di esempio lo confronta con il GUID nel tipo di connessione. A meno che i due GUID corrispondano esattamente, il grabber di esempio rifiuta la connessione.

Per i tipi di supporti video, il grabber di esempio ignora il blocco di formato. Pertanto, accetterà qualsiasi dimensione video e frequenza dei fotogrammi. Quando si chiama `SetMediaType` , impostare il blocco di formato (**pbFormat**) su **null** e la dimensione (**cbFormat**) su zero. Per i tipi di supporti audio, il grabber di esempio esaminerà la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) e richiederà l'altro filtro per la connessione a tale formato, a meno che il blocco di formato in *pType* non sia **null** o il tag format sia un formato Wave \_ \_ PCM e gli altri membri della struttura siano pari a zero.

Esempio 1:

-   Tipo principale: video di MEDIATYPE \_
-   Sottotipo: GUID \_ null
-   Tipo di formato: GUID \_ null

Il grabber di esempio accetterà qualsiasi tipo di video in cui il tipo principale è uguale a MEDIATYPE \_ video. Non controllerà il sottotipo.

Esempio 2:

-   Tipo principale: video di MEDIATYPE \_
-   Sottotipo: MEDIASUBTYPE \_ RGB24
-   Tipo di formato: GUID \_ null

A questo punto, il grabber di esempio controllerà il sottotipo e accetterà solo il video RGB 24.

**Limitazioni:** Indipendentemente dal tipo impostato, il filtro Grabber di esempio rifiuta tutti i tipi di video con orientamento dall'alto in basso ( *bialtezza* negativa) o con un tipo di formato formato \_ VideoInfo2. In questo caso, anche se il `SetMediaType` metodo ha esito positivo, il filtro non si connette.

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

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaccia ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 
