---
title: Metodo IWMDRMLicenseQuery QueryActionAllowed (Wmdrmsdk.h)
description: Il metodo QueryActionAllowed esegue una query sull'archivio licenze locale per recuperare lo stato della licenza per una o più azioni DRM che si applicano a un ID chiave specificato.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Metodo QueryActionAllowed windows Media Format
- Metodo QueryActionAllowed windows Media Format , interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery windows Media Format , metodo QueryActionAllowed
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
ms.openlocfilehash: 9f6974a04f92852ef9e56b473126eb8e0cc2d92a9bdcf5192e10abe800978bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846875"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a>Metodo IWMDRMLicenseQuery::QueryActionAllowed

Il **metodo QueryActionAllowed** esegue una query sull'archivio licenze locale per recuperare lo stato della licenza per una o più azioni DRM che si applicano a un ID chiave specificato.

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

*bstrKID* \[ Pollici\]
</dt> <dd>

ID chiave per cui eseguire una query. Verranno valutate solo le licenze che si applicano a questo ID chiave.

</dd> <dt>

*bstrMinReqIndivVersion* \[ Pollici\]
</dt> <dd>

Versione minima di sicurezza specificata nell'intestazione del file ASF. Questo parametro è facoltativo. Passare **NULL** per eseguire la query senza queste informazioni.

</dd> <dt>

*cActionsToQuery* \[ Pollici\]
</dt> <dd>

Numero di azioni per cui eseguire una query. Questo valore deve essere impostato sul numero di elementi nelle matrici passate per i parametri *rgbstrActionsToQuery* e *rgdwQueryResult.*

</dd> <dt>

*rgbstrActionsToQuery \[ \]* \[in\]
</dt> <dd>

Matrice di uno o più diritti per cui eseguire una query. Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*. Ogni elemento deve essere impostato su una delle costanti seguenti:



| Costante                                         | Descrizione                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ActionAllowed \_ Playback             | Includere per eseguire una query per ottenere il diritto di riprodurre il contenuto.                              |
| g \_ wszWMDRM \_ ActionAllowed \_ Copy                 | Includere per eseguire una query per ottenere il diritto di copiare il contenuto in dispositivi o supporti esterni. |
| g \_ wszWMDRM \_ ActionAllowed \_ Playlist         | Includere per eseguire una query per ottenere il diritto di copiare il contenuto in CD come parte di una playlist.  |
| g \_ wszWMDRM \_ ActionAllowed \_ CreateThumbnailImage | Includere per eseguire una query per ottenere il diritto di creare un'immagine di anteprima dal contenuto.     |
| g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD             | Includere per eseguire una query per ottenere il diritto di copiare il contenuto in CD.                        |



 

</dd> <dt>

*rgdwQueryResult \[ \]* \[out\]
</dt> <dd>

Matrice di una o più variabili DWORD che ricevono i risultati della query per i diritti specificati da *rgbstrActionsToQuery*. Se è consentita un'azione, l'elemento corrispondente viene impostato su zero. Se un'azione non è consentita, l'elemento viene impostato su uno o più valori dell'enumerazione [**DRM \_ ACTION ALLOWED QUERY \_ \_ \_ RESULTS**](drm-action-allowed-query-results.md) combinata tramite l'operazione OR bit per bit. Questa matrice deve contenere il numero di elementi specificato da *cActionsToQuery*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si esegue una query per i diritti di riproduzione e copia, si otterrà risultati più accurati impostando prima i parametri ambientali. Usare il [**metodo SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) per impostare i parametri ambientali. I risultati delle query per il diritto di masterizzazione non sono interessati dai parametri ambientali. è possibile usare in modo sicuro le impostazioni predefinite.

I risultati restituiti dal **metodo QueryActionAllowed** vengono aggregati da zero o più licenze nell'archivio licenze locale. Il metodo potrebbe non cercare tutte le licenze che si applicano all'ID chiave se rileva un risultato abilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Esecuzione di query per informazioni sui diritti semplici**](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





