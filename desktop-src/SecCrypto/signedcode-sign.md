---
description: Crea una firma digitale Authenticode e firma il file eseguibile specificato nella proprietà SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Metodo SignedCode. Sign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331267"
---
# <a name="signedcodesign-method"></a>Metodo SignedCode. Sign

\[Il metodo **Sign** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

Il metodo **Sign** crea una firma digitale Authenticode e firma il file eseguibile specificato nella proprietà [**SignedCode. FileName**](signedcode-filename.md) .

## <a name="syntax"></a>Sintassi


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Firmatario* \[ in, facoltativo\]
</dt> <dd>

Oggetto [**firmatario**](signer.md) che ha accesso alla chiave privata del certificato utilizzato per firmare il codice. Il valore predefinito è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Prima che venga chiamato il metodo **Sign** , il file che contiene il codice deve essere specificato nella proprietà [**filename**](signedcode-filename.md) .

Se il file eseguibile è già firmato, questo metodo sovrascrive la firma esistente.

I risultati seguenti si applicano al valore del parametro del *firmatario* :

-   Se il parametro del *firmatario* non è **null**, questo metodo usa la chiave privata a cui fa riferimento il certificato associato per crittografare la firma. Se la chiave privata a cui fa riferimento il certificato non è disponibile, il metodo ha esito negativo.
-   Se il parametro del *firmatario* è **null** ed è presente esattamente un certificato nell' \_ archivio My Store che ha accesso a una chiave privata con funzionalità di firma del codice, il certificato viene usato per creare la firma.
-   Se il parametro del *firmatario* è **null**, il valore della proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è true ed esiste più di un certificato nell' \_ archivio My dell'utente corrente con una chiave privata disponibile con funzionalità di firma del codice, viene visualizzata una finestra di dialogo che consente all'utente di selezionare il certificato usato.
-   Se il parametro del *firmatario* è **null** e la proprietà [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) è false, il metodo ha esito negativo.
-   Se il parametro del *firmatario* è **null** e non sono presenti certificati nell' \_ utente corrente My Store con una chiave privata disponibile con funzionalità di firma del codice, il metodo ha esito negativo.

Questo metodo usa l'algoritmo di hash SHA-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
