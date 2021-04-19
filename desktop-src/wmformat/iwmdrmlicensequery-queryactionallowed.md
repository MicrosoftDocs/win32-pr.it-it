---
title: Metodo IWMDRMLicenseQuery QueryActionAllowed (wmdrmsdk. h)
description: Il metodo QueryActionAllowed esegue una query sull'archivio licenze locale per recuperare lo stato della licenza per una o più azioni DRM applicabili a un ID chiave specificato.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Metodo QueryActionAllowed Windows Media Format
- Metodo QueryActionAllowed Windows Media Format, interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, metodo QueryActionAllowed
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329269"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>Metodo IWMDRMLicenseQuery:: QueryActionAllowed

Il metodo **QueryActionAllowed** esegue una query sull'archivio licenze locale per recuperare lo stato della licenza per una o più azioni DRM applicabili a un ID chiave specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKID* \[ in\]
</dt> <dd>

ID chiave per cui eseguire una query. Verranno valutate solo le licenze che si applicano a questo ID chiave.

</dd> <dt>

*bstrMinReqIndivVersion* \[ in\]
</dt> <dd>

Versione di sicurezza minima specificata nell'intestazione del file ASF. Questo parametro è facoltativo. Passare **null** per eseguire la query senza queste informazioni.

</dd> <dt>

*cActionsToQuery* \[ in\]
</dt> <dd>

Il numero di azioni per cui eseguire una query. Questo valore deve essere impostato sul numero di elementi nelle matrici passate per i parametri *rgbstrActionsToQuery* e *rgdwQueryResult* .

</dd> <dt>

*\[ rgbstrActionsToQuery \]* \[in\]
</dt> <dd>

Matrice di uno o più diritti per i quali eseguire una query. Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*. Ogni elemento deve essere impostato su una delle seguenti costanti:



| Costante                                         | Descrizione                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ riproduzione ActionAllowed g \_ wszWMDRM             | Includere per eseguire una query per il diritto di riprodurre il contenuto.                              |
| g \_ wszWMDRM \_ ActionAllowed \_ Copy                 | Includere per eseguire una query per il diritto di copiare il contenuto in dispositivi esterni o supporti. |
| g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn         | Includere per eseguire una query per il diritto di copiare il contenuto in CD come parte di una playlist.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Includere per eseguire una query per il diritto di creare un'immagine di anteprima dal contenuto.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Includere per eseguire una query per il diritto di copiare il contenuto in CD.                        |



 

</dd> <dt>

*\[ rgdwQueryResult \]* in \[ uscita\]
</dt> <dd>

Matrice di una o più variabili DWORD che ricevono i risultati della query per i diritti specificati da *rgbstrActionsToQuery*. Se è consentita un'azione, l'elemento corrispondente viene impostato su zero. Se un'azione non è consentita, l'elemento viene impostato su uno o più valori dell'enumerazione dei [**\_ \_ \_ \_ risultati delle query consentiti dell'azione DRM**](drm-action-allowed-query-results.md) combinati tramite l'operazione OR bit per bit. Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si eseguono query sui diritti di riproduzione e copia, si otterranno risultati più accurati impostando prima i parametri ambientali. Usare il metodo [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) per impostare i parametri ambientali. I risultati delle query per il diritto Burn non sono interessati dai parametri ambientali; è possibile usare in modo sicuro le impostazioni predefinite.

I risultati restituiti dal metodo **QueryActionAllowed** sono aggregati da zero o più licenze nell'archivio licenze locale. Il metodo non può eseguire ricerche in tutte le licenze valide per l'ID chiave se viene rilevato un risultato abilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Esecuzione di query per ottenere informazioni semplici sui diritti**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





