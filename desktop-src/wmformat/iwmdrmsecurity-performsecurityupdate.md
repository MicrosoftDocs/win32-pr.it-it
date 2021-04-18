---
title: Metodo IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: Il metodo PerformSecurityUpdate avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer locale.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Metodo PerformSecurityUpdate Windows Media Format
- Metodo PerformSecurityUpdate Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325535"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity::P metodo erformSecurityUpdate

Il metodo **PerformSecurityUpdate** avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Opzione di aggiornamento espressa come uno dei flag seguenti.



| Flag                                          | Descrizione                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| sicurezza di WMDRM \_ \_ eseguire \_ indiv               | Fa in modo che il componente DRM venga individualizzato solo se la versione del client non è aggiornata. |
| \_sicurezza WMDRM \_ eseguire l' \_ aggiornamento delle revoche \_ | Causa l'aggiornamento degli elenchi di revoche nel computer client.                               |
| WMDRM \_ Security \_ esegue \_ Force \_ indiv        | Fa in modo che il componente DRM venga individualizzato anche se la versione del client è aggiornata.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a un oggetto che può essere utilizzato per annullare questa operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Viene restituito immediatamente dopo la chiamata di e quindi genera eventi a seconda del flag impostato nel parametro *dwFlags* .

Per l'individualizzazione (flag impostato su WMDRM \_ Security eseguire \_ \_ indiv o WMDRM \_ Security \_ Esegui \_ Force \_ indiv), una serie di eventi **MEWMDRMIndividualizationProgress** viene generata seguito da un evento **MEWMDRMIndividualizationCompleted** al termine dell'elaborazione. Il valore di ogni evento **MEWMDRMIndividualizationProgress** ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** . È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .

Per aggiornare gli elenchi di revoche (flag impostato su WMDRM \_ Security \_ eseguire l' \_ aggiornamento delle revoche \_ ), viene generato un evento **MEWMDRMREvocationDownloadCompleted** al termine dell'elaborazione.

> [!Note]  
> Quando **PerformSecurityUpdate** completa l'individualizzazione, gli unici oggetti esistenti che riflettono il nuovo stato individualizzato sono quelli che ereditano da **IWMDRMSecurity**. Tutti gli altri oggetti esistenti non verranno aggiornati. È necessario rilasciare e ricreare altri oggetti in modo che riflettano il nuovo stato individualizzato.

 

Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Revoca e rinnovo automatici dei componenti**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**Esecuzione dell'individualizzazione DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





