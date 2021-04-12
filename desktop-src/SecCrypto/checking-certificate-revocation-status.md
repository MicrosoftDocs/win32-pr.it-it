---
description: Per impostazione predefinita, CAPICOM non Abilita il controllo delle revoche di certificati.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Verifica dello stato di revoca dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232795"
---
# <a name="checking-certificate-revocation-status"></a>Verifica dello stato di revoca dei certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Per impostazione predefinita, CAPICOM non Abilita il controllo delle revoche di certificati. Tuttavia, la verifica delle revoche di certificati può essere abilitata a livello di codice per un determinato certificato tramite la proprietà **IsValid. CheckFlag** di un oggetto certificato. Dopo aver impostato il valore appropriato di **CheckFlag** , l'accesso alla proprietà **IsValid. Result** dell'oggetto certificato o la compilazione del percorso di verifica del certificato mediante il metodo di compilazione di un oggetto chain impone il controllo delle revoche.

Nell'esempio seguente è stata creata un'istanza di CERT come certificato di CAPICOM valido.


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



Il valore precedente si applica a un certificato singolo, indipendentemente dal modo in cui è stato ottenuto. L'esecuzione del controllo delle revoche sui certificati in un oggetto [**SignedData**](signeddata.md) non è diversa perché il metodo [**Verify**](signeddata-verify.md) dell'oggetto **SignedData** non può essere usato a questo scopo perché l'abilitazione di CAPICOM \_ Verifica la \_ firma e il \_ \_ certificato non causa il controllo CRL.

Al contrario, è necessario impostare **CheckFlag** per ogni certificato del firmatario. Si consideri l'esempio seguente in cui è stata creata un'istanza di sData come oggetto [**SignedData**](signeddata.md) di CAPICOM valido.


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



L'esempio aggiuntivo è il ciclo su tutti i certificati nell'oggetto [**SignedData**](signeddata.md) .

 

 



