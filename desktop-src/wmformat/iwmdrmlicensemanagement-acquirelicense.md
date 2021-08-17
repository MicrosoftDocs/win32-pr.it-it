---
title: Metodo IWMDRMLicenseManagement AcquireLicense (Wmdrmsdk.h)
description: Il metodo AcquireLicense acquisisce in modo asincrono una licenza da un URL specificato.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Metodo AcquireLicense per Windows Media Format
- Metodo AcquireLicense windows Media Format , interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement windows Media Format , metodo AcquireLicense
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
ms.openlocfilehash: 3ad8251650c8a7e16c6eb2fc957df5e70459239c0cd6cf1184b5209ae51b6aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701127"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>Metodo IWMDRMLicenseManagement::AcquireLicense

Il **metodo AcquireLicense acquisisce** in modo asincrono una licenza da un URL specificato.

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

*bstrURL* \[ Pollici\]
</dt> <dd>

URL del server licenze da cui acquisire la licenza. Passare **NULL per** fare in modo che il metodo an analisi l'URL dall'intestazione del contenuto.

</dd> <dt>

*bstrHeaderData* \[ Pollici\]
</dt> <dd>

Intestazione del contenuto da passare al server licenze. Se *bstrURL* è **NULL,** il metodo an analisirà l'URL da questa intestazione. Se *dwFlags è* impostato su WMDRM ACQUIRE LICENSE LEGACY NONSILENT, impostare questo valore sull'ID chiave \_ anziché \_ \_ \_ sull'intera intestazione del contenuto.

</dd> <dt>

*bstrActions* \[ Pollici\]
</dt> <dd>

Stringa contenente zero o più azioni per cui richiedere l'autorizzazione nella licenza. La stringa deve essere formattata come segue:

-   Ogni azione deve essere definita all'interno di un elemento ACTION. I dati dell'elemento sono la stringa dell'azione.
-   Tutti gli elementi ACTION devono essere contenuti in un elemento ACTIONLIST.

    Ad esempio, la stringa per richiedere una licenza per riprodurre il contenuto è formattata come segue:

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Flag di opzione di acquisizione della licenza. Impostare su una delle costanti nella tabella seguente.



| Costante                                   | Descrizione                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ ACQUIRE \_ LICENSE \_ SILENT            | La licenza verrà rilasciata direttamente tramite Internet senza alcuna conferma da parte dell'applicazione client.              |
| WMDRM \_ ACQUIRE \_ LICENSE \_ NONSILENT         | Il sottosistema DRM creerà una richiesta di licenza che verrà restituita in modo asincrono per la pubblicazione nel server licenze. |
| WMDRM \_ ACQUIRE \_ LICENSE \_ LEGACY \_ NONSILENT | Uguale a WMDRM \_ ACQUIRE \_ LICENSE NONSILENT, ad eccezione del fatto che verrà creata una richiesta di licenza DRM versione \_ 1.           |



 

</dd> <dt>

*ppunkCancelationCookie* \[ Cambio\]
</dt> <dd>

Puntatore che riceve un puntatore **all'interfaccia IUnknown** di un oggetto che identifica questa chiamata asincrona. Questo puntatore a interfaccia può essere usato per annullare la chiamata asincrona chiamando il [**metodo IWMDRMEventGenerator::CancelAsyncOperation.**](iwmdrmeventgenerator-cancelasyncoperation.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene eseguito in modo asincrono. Restituisce immediatamente dopo essere stato chiamato e quindi genera un evento **MEWMDRMLicenseAcquisitionCompleted** al termine dell'elaborazione. Per le operazioni di acquisizione di licenze non invisibile all'utente, il valore dell'evento ottenuto chiamando **IMFMediaEvent::GetValue** è un **puntatore IUnknown.** È possibile chiamare il **metodo QueryInterface** dell'interfaccia **IUnknown** recuperata per ottenere un'istanza dell'interfaccia [**IWMDRMNonSilentLicenseAquisition.**](iwmdrmnonsilentlicenseaquisition.md)

Per altre informazioni sull'uso dei metodi asincroni delle API estese del client DRM Windows, vedere Uso del modello di Media Foundation [eventi.](using-the-media-foundation-model.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Acquisizione delle licenze invisibile all'utente**](silent-license-acquisition.md)
</dt> </dl>

 

 





