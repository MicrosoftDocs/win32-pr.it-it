---
title: Metodo PerformSecurityUpdate IWMDRMSecurity (Wmdrmsdk.h)
description: Il metodo PerformSecurityUpdate avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer locale.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Metodo PerformSecurityUpdate windows Media Format
- Metodo PerformSecurityUpdate windows Media Format , interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity windows Media Format, metodo PerformSecurityUpdate
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
ms.openlocfilehash: 8521497c1e2bca1bb2ae11349a4829c22c8b092a4cd0034008b314a7b69adb6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707901"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>Metodo IWMDRMSecurity::P erformSecurityUpdate

Il **metodo PerformSecurityUpdate** avvia un aggiornamento della sicurezza per il sottosistema DRM nel computer locale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Opzione update espressa come uno dei flag seguenti.



| Flag                                          | Descrizione                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| WMDRM \_ SECURITY \_ PERFORM \_ INDIV               | Fa sì che il componente DRM sia individualizzato solo se la versione del client non è aggiornata. |
| LA SICUREZZA DI WMDRM \_ \_ ESEGUE \_ L'AGGIORNAMENTO DELLE \_ REVOCHE | Determina l'aggiornamento degli elenchi di revoche nel computer client.                               |
| WMDRM \_ SECURITY \_ PERFORM \_ FORCE \_ INDIV        | Fa sì che il componente DRM sia individualizzato anche se la versione del client è aggiornata.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a un oggetto che può essere utilizzato per annullare questa operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Restituisce immediatamente dopo essere stato chiamato e quindi genera eventi a seconda del flag impostato nel *parametro dwFlags.*

Per la individualizzazione (flag impostato su WMDRM SECURITY PERFORM INDIV o WMDRM SECURITY PERFORM FORCE INDIV), una serie di eventi \_ \_ \_ \_ \_ \_ \_ **MEWMDRMIndividualizationProgress** viene generata seguita da un evento **MEWMDRMIndividualizationCompleted** al termine dell'elaborazione. Il valore di ogni evento **MEWMDRMIndividualizationProgress** ottenuto chiamando **IMFMediaEvent::GetValue** è un **puntatore IUnknown.** È possibile chiamare il **metodo QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza [**dell'interfaccia IWMDRMIndividualizationStatus.**](iwmdrmindividualizationstatus.md)

Per aggiornare gli elenchi di revoche (flag impostato su WMDRM SECURITY PERFORM REVOCATION REFRESH), viene generato un evento \_ \_ \_ \_ **MEWMDRMREvocationDownloadCompleted** al termine dell'elaborazione.

> [!Note]  
> Quando **PerformSecurityUpdate completa** l'individualizzazione, gli unici oggetti esistenti che rifletteranno il nuovo stato individualizzato sono quelli che ereditano da **IWMDRMSecurity.** Tutti gli altri oggetti esistenti non verranno aggiornati. È necessario rilasciare e creare nuovamente tutti gli altri oggetti in modo che riflettano il nuovo stato individualizzato.

 

Per altre informazioni sull'uso dei metodi asincroni delle API estese del client DRM Windows, vedere Uso del modello di Media Foundation [eventi.](using-the-media-foundation-model.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Revoca e rinnovo automatici dei componenti**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**Esecuzione della individualizzazione DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





