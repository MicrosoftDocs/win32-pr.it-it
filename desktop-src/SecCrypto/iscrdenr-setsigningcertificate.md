---
description: Specifica un certificato di firma (noto anche come certificato dell'agente di registrazione).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Metodo ISCrdEnr:: setSigningCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319358"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>Metodo ISCrdEnr:: setSigningCertificate

Il metodo **setSigningCertificate** specifica un certificato di firma (noto anche come *certificato dell'agente di registrazione*).

Prima di eseguire la registrazione per conto di utenti, è necessario selezionare o impostare un certificato di firma. La [*chiave privata*](../secgloss/p-gly.md) associata a questo certificato di firma viene usata per firmare una \# richiesta PKCS 7. PKCS \# 7, a sua volta, contiene la richiesta PKCS 10 dell'utente \# (che è firmata con la chiave privata dell'utente).

## <a name="syntax"></a>Sintassi


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
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

Nome del modello di certificato per il certificato di firma. Se è stato ottenuto un certificato EnrollmentAgent, è possibile usare il valore "EnrollmentAgent".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="remarks"></a>Commenti

Prima di eseguire la registrazione per conto di un utente, è innanzitutto necessario ottenere un certificato di firma. È possibile ottenere un certificato di firma tramite lo snap-in MMC di gestione certificati. Il metodo **setSigningCertificate** non ottiene il certificato di firma ma informa il controllo di registrazione della smart card che in precedenza ha ottenuto il certificato di firma da usare. Il metodo **setSigningCertificate** Cerca nell'archivio "My" del chiamante il certificato di firma più recente corrispondente al modello di certificato specificato da *bstrCertTemplateName*.

Un'alternativa a **setSigningCertificate** è **ISCrdEnr:: setSigningCertificate**.

Dopo aver impostato un certificato di firma, è possibile recuperarne il nome chiamando [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

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

 

 
