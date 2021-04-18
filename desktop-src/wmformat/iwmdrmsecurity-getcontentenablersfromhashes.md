---
title: Metodo IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: Il metodo GetContentEnablersFromHashes recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati con hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Metodo GetContentEnablersFromHashes Windows Media Format
- Metodo GetContentEnablersFromHashes Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325539"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a>Metodo IWMDRMSecurity:: GetContentEnablersFromHashes

Il metodo **GetContentEnablersFromHashes** recupera le interfacce di attivazione del contenuto che consentono il rinnovo dei componenti in base ai certificati con hash.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rgpbCertHashes* \[ in\]
</dt> <dd>

Matrice di hash del certificato per ottenere gli abilitatori del contenuto per.

</dd> <dt>

*cCerts* \[ in\]
</dt> <dd>

Numero di certificati per i quali recuperare gli abilitatori del contenuto. Questo è il numero di elementi nella matrice *rgpbCertHashes* .

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

[**Interfaccia IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





