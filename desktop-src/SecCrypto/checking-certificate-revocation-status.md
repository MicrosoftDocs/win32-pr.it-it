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
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="1f73d-103">Verifica dello stato di revoca dei certificati</span><span class="sxs-lookup"><span data-stu-id="1f73d-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="1f73d-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1f73d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1f73d-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1f73d-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="1f73d-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="1f73d-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="1f73d-107">Per impostazione predefinita, CAPICOM non Abilita il controllo delle revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="1f73d-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="1f73d-108">Tuttavia, la verifica delle revoche di certificati può essere abilitata a livello di codice per un determinato certificato tramite la proprietà **IsValid. CheckFlag** di un oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="1f73d-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="1f73d-109">Dopo aver impostato il valore appropriato di **CheckFlag** , l'accesso alla proprietà **IsValid. Result** dell'oggetto certificato o la compilazione del percorso di verifica del certificato mediante il metodo di compilazione di un oggetto chain impone il controllo delle revoche.</span><span class="sxs-lookup"><span data-stu-id="1f73d-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="1f73d-110">Nell'esempio seguente è stata creata un'istanza di CERT come certificato di CAPICOM valido.</span><span class="sxs-lookup"><span data-stu-id="1f73d-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


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



<span data-ttu-id="1f73d-111">Il valore precedente si applica a un certificato singolo, indipendentemente dal modo in cui è stato ottenuto.</span><span class="sxs-lookup"><span data-stu-id="1f73d-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="1f73d-112">L'esecuzione del controllo delle revoche sui certificati in un oggetto [**SignedData**](signeddata.md) non è diversa perché il metodo [**Verify**](signeddata-verify.md) dell'oggetto **SignedData** non può essere usato a questo scopo perché l'abilitazione di CAPICOM \_ Verifica la \_ firma e il \_ \_ certificato non causa il controllo CRL.</span><span class="sxs-lookup"><span data-stu-id="1f73d-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="1f73d-113">Al contrario, è necessario impostare **CheckFlag** per ogni certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="1f73d-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="1f73d-114">Si consideri l'esempio seguente in cui è stata creata un'istanza di sData come oggetto [**SignedData**](signeddata.md) di CAPICOM valido.</span><span class="sxs-lookup"><span data-stu-id="1f73d-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


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



<span data-ttu-id="1f73d-115">L'esempio aggiuntivo è il ciclo su tutti i certificati nell'oggetto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="1f73d-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



