---
description: Recupera la raccolta di certificati nel file eseguibile firmato.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: Proprietà SignedCode. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329463"
---
# <a name="signedcodecertificates-property"></a>Proprietà SignedCode. Certificates

\[La proprietà **Certificates** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

La proprietà **Certificates** recupera la raccolta di certificati nel file eseguibile firmato.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a>Valore proprietà

Raccolta di [**certificati**](certificates.md) che contiene tutti i certificati nel file eseguibile firmato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
