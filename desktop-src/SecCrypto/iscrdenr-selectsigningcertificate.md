---
description: Consente di visualizzare una finestra di dialogo Seleziona certificato, in cui è possibile selezionare un certificato di firma (noto anche come certificato agente di registrazione).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Metodo ISCrdEnr:: selectSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884850"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>Metodo ISCrdEnr:: selectSigningCertificate

Il metodo **selectSigningCertificate** Visualizza una finestra di dialogo **Seleziona certificato** , che consente di selezionare un certificato di firma (noto anche come *certificato agente di registrazione*).

Prima di eseguire la registrazione per conto di utenti, è necessario selezionare un certificato di firma. La [*chiave privata*](../secgloss/p-gly.md) associata a questo certificato di firma viene usata per firmare una \# richiesta PKCS 7. PKCS \# 7, a sua volta, contiene la richiesta PKCS 10 dell'utente \# (che è firmata con la chiave privata dell'utente).

## <a name="syntax"></a>Sintassi


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Riservato per utilizzi futuri. Impostare questo valore su zero.

</dd> <dt>

*bstrCertTemplateName* \[ in\]
</dt> <dd>

Stringa che rappresenta il nome del modello di certificato per il certificato di firma. Se è stato ottenuto un certificato EnrollmentAgent, è possibile usare il valore "EnrollmentAgent".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce **S \_ OK**.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Prima di eseguire la registrazione per conto di un utente, è innanzitutto necessario ottenere un certificato di firma. È possibile ottenere un certificato di firma tramite lo snap-in MMC di gestione certificati. Il metodo **selectSigningCertificate** non ottiene il certificato di firma ma Visualizza una finestra di dialogo dei certificati di firma ottenuti in precedenza, consentendo di scegliere il certificato che verrà usato per firmare le richieste di registrazione per conto dell'utente.

Un'alternativa a **selectSigningCertificate** è [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).

Dopo aver selezionato un certificato di firma, è possibile recuperarne il nome chiamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
