---
description: Richiede un endpoint utilizzato per connettersi a un servizio.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Metodo IUpdateEndpointProvider:: getserviceendpoint (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307624"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>Metodo IUpdateEndpointProvider:: getserviceendpoint

Richiede un endpoint utilizzato per connettersi a un servizio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ServiceID* \[ in\]
</dt> <dd>

Identifica il servizio da aggiornare.

</dd> <dt>

*EndpointType* \[ in\]
</dt> <dd>

Identifica il tipo di endpoint implementato dal servizio.

L'enumerazione [**UpdateEndpointType**](updateendpointtype.md) definisce le costanti seguenti.

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**


</dt> <dd>

Endpoint client-server utilizzato per la connessione al servizio di aggiornamento.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**


</dt> <dd>

Un endpoint di Reporting utilizzato quando il client segnala i risultati di analisi, download e installazioni di nuovo nel servizio di aggiornamento

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**


</dt> <dd>

Un endpoint Self-Update utilizzato quando il computer client contatta un servizio di aggiornamento per verificare se è presente una nuova versione del software client di Windows Update Agent.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**


</dt> <dd>

Un endpoint del regolamento utilizzato quando il computer client contatta il servizio di regolamentazione per agire su un particolare aggiornamento applicabile al computer di destinazione.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**


</dt> <dd>

Un Simple-Targeting che viene utilizzato solo con servizi privati (server WSUS negli ambienti aziendali).

</dd> </dl> </dd> <dt>

*proxySettings* \[ in\]
</dt> <dd>

Identifica le impostazioni utilizzate per la connessione a un server proxy.

</dd> <dt>

*hUserToken* \[ in\]
</dt> <dd>

Contiene un oggetto handle di token che rappresenta l'utente. Il provider di endpoint utilizza questo token per determinare quali impostazioni e credenziali del proxy utilizzare.

</dd> <dt>

*fRefreshOnline* \[ in\]
</dt> <dd>

Indica che WUA Weather richiede un nuovo token. True indica che è richiesto un nuovo token. False indica che è richiesto un token nuovo o memorizzato nella cache. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*pbstrEndpointLoc* \[ out\]
</dt> <dd>

Specificare l'URL usato per comunicare con il servizio. Per un endpoint sicuri-server, ad esempio, si tratta dell'URL del servizio server client. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se ha esito positivo. In caso contrario, restituisce un codice di errore COM o Windows.

## <a name="remarks"></a>Commenti

WUA imposta in genere il parametro *fRefreshOnline* su false quando il metodo viene chiamato per la prima volta, quindi se si verifica un errore di connessione WUA imposta tale parametro su true quando il metodo viene chiamato nuovamente. Tuttavia, l'implementazione di questo metodo può richiedere un nuovo token da un servizio token di sicurezza (STS) o fornire un token memorizzato nella cache in qualsiasi momento.

Se l'endpoint non richiede l'autenticazione, il chiamante può connettersi al servizio usando solo l'URL specificato dal parametro *pbstrEndpointLoc* .

Se l'endpoint necessita di autenticazione, il chiamante può usare l'URL specificato dal parametro *pbstrEndpointLoc* e i dati forniti dagli altri parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>                   |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>                |
| Intestazione<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUpdateEndpointProvider**](iupdateendpointprovider.md)
</dt> </dl>

 

 




