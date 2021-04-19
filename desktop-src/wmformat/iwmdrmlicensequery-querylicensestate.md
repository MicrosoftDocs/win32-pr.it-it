---
title: Metodo IWMDRMLicenseQuery QueryLicenseState (wmdrmsdk. h)
description: Il metodo QueryLicenseState esegue una query nell'archivio licenze locale per ottenere informazioni sulle licenze che si applicano a un ID chiave per uno o più diritti specifici.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Metodo QueryLicenseState Windows Media Format
- Metodo QueryLicenseState Windows Media Format, interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, metodo QueryLicenseState
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325559"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>Metodo IWMDRMLicenseQuery:: QueryLicenseState

Il metodo **QueryLicenseState** esegue una query nell'archivio licenze locale per ottenere informazioni sulle licenze che si applicano a un ID chiave per uno o più diritti specifici.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ in\]
</dt> <dd>

ID chiave per cui eseguire una query. Verranno valutate solo le licenze che si applicano a questo ID chiave.

</dd> <dt>

*cActionsToQuery* \[ in\]
</dt> <dd>

Il numero di azioni per cui eseguire una query. Questo valore deve essere impostato sul numero di elementi nelle matrici passate per i parametri *rgbstrActionsToQuery* e *rgResultStateData* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[in\]
</dt> <dd>

Matrice di uno o più diritti per i quali eseguire una query. Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*. Ogni elemento deve essere impostato su una delle seguenti costanti.



| Costante                                        | Descrizione                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ LicenseState \_ backup               | Includere per eseguire una query per informazioni dettagliate sul diritto di eseguire il backup e il ripristino della licenza.                                                               |
| g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | Includere per eseguire una query per informazioni dettagliate sul diritto di condividere il contenuto con un gruppo di utenti come parte di uno scenario di riproduzione collaborativo.          |
| g \_ wszWMDRM \_ LicenseState \_ Copy                 | Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in dispositivi esterni o supporti.                                                 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in CD.                                                                        |
| g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in un dispositivo che non supporta l'iniziativa Secure Digital Media Initiative (SDMI). |
| g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in un dispositivo che supporta SDMI.                                           |
| g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage | Includere per eseguire una query per informazioni dettagliate sul diritto di creare un'immagine di anteprima dal contenuto.                                                     |
| \_ \_ riproduzione LicenseState g \_ wszWMDRM             | Includere per eseguire una query per informazioni dettagliate sul diritto di riprodurre il contenuto.                                                                              |
| g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | Includere per eseguire una query per informazioni dettagliate sul diritto di copiare il contenuto in CD come parte di una playlist.                                                  |



 

</dd> <dt>

*\[ rgResultStateData \]* in \[ uscita\]
</dt> <dd>

Matrice di una o più strutture di [**dati di \_ stato delle licenze \_ \_ DRM**](drmdrm-license-state-data.md) che ricevono le informazioni sullo stato della licenza che si applicano a destra nell'elemento corrispondente del parametro *rgbstrActionsToQuery* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Verrà eseguita la ricerca e la valutazione di tutte le licenze valide per l'ID chiave specificato. I risultati sono aggregati, pertanto ogni **struttura \_ \_ \_ dei dati di stato delle licenze DRM** può contenere informazioni di più licenze.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





