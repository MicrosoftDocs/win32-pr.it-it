---
description: CAPICOM non abilita il controllo delle revoche di certificati per impostazione predefinita.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Controllo dello stato di revoca del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf1ce98e392da94fd800316fe63c5b79c8572a319c6db4246e7907eb80966d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769540"
---
# <a name="checking-certificate-revocation-status"></a>Controllo dello stato di revoca del certificato

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

CAPICOM non abilita il controllo delle revoche di certificati per impostazione predefinita. Tuttavia, il controllo delle revoche di certificati può essere abilitato a livello di codice per un determinato certificato tramite la proprietà **IsValid.CheckFlag** di un oggetto Certificate. Dopo aver impostato il valore appropriato di **CheckFlag,** l'accesso alla proprietà **IsValid.Result** dell'oggetto Certificate o la compilazione del percorso di verifica del certificato usando il metodo Build di un oggetto Chain forza il controllo delle revoche.

Nell'esempio seguente è stata creata un'istanza di cert come certificato CAPICOM valido.


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



Il precedente si applica a un singolo certificato, indipendentemente dal modo in cui è stato ottenuto. L'esecuzione del controllo delle revoche sui certificati in un oggetto [**SignedData**](signeddata.md) non è diversa perché il metodo [**Verify**](signeddata-verify.md) dell'oggetto **SignedData** non può essere usato a questo scopo perché l'abilitazione di CAPICOM VERIFY SIGNATURE AND CERTIFICATE non causa il controllo \_ \_ \_ \_ CRL.

È invece **necessario impostare CheckFlag** per il certificato di ogni firmatario. Si consideri l'esempio seguente in cui è stata creata un'istanza di sData come oggetto [**SIGNEDData**](signeddata.md) CAPICOM valido.


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



L'esempio aggiuntivo è il ciclo su tutti i certificati [**nell'oggetto SignedData.**](signeddata.md)

 

 



