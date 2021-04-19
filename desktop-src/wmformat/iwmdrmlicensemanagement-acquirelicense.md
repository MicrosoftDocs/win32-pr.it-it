---
title: Metodo IWMDRMLicenseManagement AcquireLicense (wmdrmsdk. h)
description: Il metodo AcquireLicense acquisisce in modo asincrono una licenza da un URL specificato.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Metodo AcquireLicense Windows Media Format
- Metodo AcquireLicense Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327468"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>Metodo IWMDRMLicenseManagement:: AcquireLicense

Il metodo **AcquireLicense** acquisisce in modo asincrono una licenza da un URL specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrURL* \[ in\]
</dt> <dd>

URL del server licenze da cui acquisire la licenza. Passare **null** per fare in modo che il metodo analizzi l'URL dall'intestazione del contenuto.

</dd> <dt>

*bstrHeaderData* \[ in\]
</dt> <dd>

Intestazione del contenuto da passare al server licenze. Se *bstrURL* è **null**, il metodo analizzerà l'URL da questa intestazione. Se *dwFlags* è impostato su WMDRM \_ acquisisce \_ License \_ legacy \_ Unsilent, impostare questo valore sull'ID chiave anziché sull'intera intestazione Content.

</dd> <dt>

*bstrActions* \[ in\]
</dt> <dd>

Stringa contenente zero o più azioni per le quali richiedere l'autorizzazione per la licenza. La stringa deve essere formattata come indicato di seguito:

-   Ogni azione deve essere definita all'interno di un elemento ACTION. I dati dell'elemento sono la stringa dell'azione.
-   Tutti gli elementi ACTION devono essere contenuti all'interno di un elemento ACTION.

    Ad esempio, la stringa per richiedere una licenza per riprodurre il contenuto è formattata come la seguente:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flag dell'opzione di acquisizione delle licenze. Impostare su una delle costanti nella tabella seguente.



| Costante                                   | Descrizione                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ acquisire la \_ licenza \_ invisibile all'utente            | La licenza verrà emessa direttamente tramite Internet senza alcuna conferma da parte dell'applicazione client.              |
| WMDRM \_ Acquisisci \_ licenza non \_ invisibile         | Il sottosistema DRM creerà una richiesta di licenza che verrà restituita in modo asincrono per la pubblicazione nel server licenze. |
| WMDRM \_ acquisire la \_ licenza \_ legacy non invisibile all' \_ utente | Analogamente a WMDRM \_ , Acquisisci \_ licenza \_ non invisibile ad eccezione del fatto che verrà creata una richiesta di licenza di DRM versione 1.           |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Puntatore che riceve un puntatore all'interfaccia **IUnknown** di un oggetto che identifica la chiamata asincrona. Questo puntatore di interfaccia può essere utilizzato per annullare la chiamata asincrona chiamando il metodo [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Viene restituito immediatamente dopo la chiamata di e quindi genera un evento **MEWMDRMLicenseAcquisitionCompleted** al termine dell'elaborazione. Per le operazioni di acquisizione di licenze non Silent, il valore dell'evento ottenuto chiamando **IMFMediaEvent:: GetValue** è un puntatore **IUnknown** . È possibile chiamare il metodo **QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .

Per ulteriori informazioni sull'utilizzo dei metodi asincroni delle API estese del client Windows Media DRM, vedere [utilizzo del modello di eventi Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Acquisizione di una licenza invisibile all'utente**](silent-license-acquisition.md)
</dt> </dl>

 

 





