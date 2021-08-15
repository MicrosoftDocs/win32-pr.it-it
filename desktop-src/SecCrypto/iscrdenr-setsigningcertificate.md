---
description: Specifica un certificato di firma (noto anche come certificato dell'agente di registrazione).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: Metodo ISCrdEnr::setSigningCertificate
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
ms.openlocfilehash: 8b93e2b76e46ed75abcd6460f351dfc2780826c2ff5e7dc8d07e8d48ae617e4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425731"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>Metodo ISCrdEnr::setSigningCertificate

Il **metodo setSigningCertificate** specifica un certificato di firma (noto anche come certificato *dell'agente di registrazione).*

Prima di eseguire la registrazione per conto degli utenti, è necessario selezionare o impostare un certificato di firma. La [*chiave privata*](../secgloss/p-gly.md) associata a questo certificato di firma viene usata per firmare una richiesta PKCS \# 7. PkcS 7, a sua volta, contiene la richiesta \# PKCS 10 dell'utente (firmata con la chiave \# privata dell'utente).

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

*dwFlags* \[ Pollici\]
</dt> <dd>

Riservato per utilizzi futuri. Impostare questo valore su zero.

</dd> <dt>

*bstrCertTemplateName* \[ Pollici\]
</dt> <dd>

Nome del modello di certificato per il certificato di firma. È possibile usare il valore "EnrollmentAgent" se è stato ottenuto un certificato EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="vb"></a>VB

Se il metodo ha esito positivo, il metodo restituisce S \_ OK.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

## <a name="remarks"></a>Commenti

Prima di eseguire la registrazione per conto di un utente, è necessario ottenere un certificato di firma. È possibile ottenere un certificato di firma utilizzando lo snap-in MMC Gestione certificati. Il **metodo setSigningCertificate** non ottiene il certificato di firma, ma comunica al controllo di registrazione smart card il certificato di firma ottenuto in precedenza da usare. Il **metodo setSigningCertificate** cerca nell'archivio "My" del chiamante il certificato di firma più recente corrispondente al modello di certificato specificato da *bstrCertTemplateName*.

Un'alternativa **a setSigningCertificate** **è ISCrdEnr::setSigningCertificate**.

Dopo aver impostato un certificato di firma, è possibile recuperarne il nome chiamando [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr è definito come 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
