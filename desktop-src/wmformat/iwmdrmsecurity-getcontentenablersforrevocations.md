---
title: Metodo IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: Il metodo GetContentEnablersForRevocations recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Metodo GetContentEnablersForRevocations Windows Media Format
- Metodo GetContentEnablersForRevocations Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327461"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a>Metodo IWMDRMSecurity:: GetContentEnablersForRevocations

Il metodo **GetContentEnablersForRevocations** recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati revocati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rgpbCerts* \[ in\]
</dt> <dd>

Matrice di certificati per cui recuperare gli abilitatori del contenuto. Il numero di elementi nella matrice deve essere specificato da *cCerts*.

</dd> <dt>

*rgpdwCertSizes* \[ in\]
</dt> <dd>

Matrice contenente le dimensioni dei certificati nella matrice *rgpbCerts* . Il numero di elementi nella matrice deve essere specificato da *cCerts*.

</dd> <dt>

*rgpguidCerts* \[ in\]
</dt> <dd>

Matrice contenente i tipi di certificati nella matrice *rgpbCerts* . Il numero di elementi nella matrice deve essere specificato da *cCerts*. Per ogni elemento della matrice, usare uno dei valori seguenti.



| Costante GUID                 | Descrizione                                                    |
|-------------------------------|----------------------------------------------------------------|
| \_app WMDRM REVOCATIONTYPE \_    | Specifica un certificato dell'applicazione.                          |
| \_dispositivo REVOCATIONTYPE \_ WMDRM | Specifica un certificato del dispositivo.                                |
| WMDRM \_ REVOCATIONTYPE \_ Cardea | Specifica un certificato Windows Media DRM per i dispositivi di rete. |



 

</dd> <dt>

*cCerts* \[ in\]
</dt> <dd>

Numero di certificati per i quali recuperare gli abilitatori del contenuto. Questo è il numero di elementi nella matrice *rgpbCerts* , la matrice *rgpdwCertSizes* e la matrice *rgpguidCerts* .

</dd> <dt>

*hResultHint* \[ in\]
</dt> <dd>

Valore restituito ricevuto dall'operazione non riuscita a causa di un certificato revocato. Se non si chiama in risposta a una chiamata al metodo non riuscita, impostare su S \_ OK.

</dd> <dt>

*prgContentEnablers* \[ out\]
</dt> <dd>

Matrice che riceve gli indirizzi delle interfacce **IMFContentEnabler** appena create. Impostare su **null** per ottenere il numero di abilitatori del contenuto nel parametro *pcContentEnablers* .

</dd> <dt>

*pcContentEnablers* \[ in uscita\]
</dt> <dd>

Numero di elementi nella matrice *prgContentEnablers* . Se *prgContentEnablers* è **null**, questo valore viene impostato sul numero di abilitatori di contenuto necessari nell'output.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se si utilizza l'interfaccia **IMFContentEnabler** per rinnovare i componenti revocati, è necessario chiarire il processo all'utente. Questo chiarimento deve essere effettuato perché il processo di aggiornamento Invia le informazioni dal computer client a un sito Web Microsoft.

Quando si chiama **IMFContentEnabler:: AutomaticEnable**, l'attivatore del contenuto avvia il browser predefinito con l'indirizzo del servizio di aggiornamento sul sito Web Microsoft. Un identificatore univoco che identifica il componente revocato viene inviato al servizio di aggiornamento. Il servizio reindirizza quindi il browser a una pagina Web da cui l'utente potrebbe essere in grado di scaricare e installare la nuova versione del componente revocato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Revoca e rinnovo automatici dei componenti**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





