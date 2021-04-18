---
description: Crea una firma di timestamp Authenticode sul file eseguibile firmato specificato nella proprietà SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode. timestamp, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327895"
---
# <a name="signedcodetimestamp-method"></a>SignedCode. timestamp, metodo

\[Il metodo **timestamp** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

Il metodo **timestamp** crea una firma timestamp Authenticode sul file eseguibile firmato specificato nella proprietà **SignedCode. FileName** . Questo timestamp è una firma del contatore nel file eseguibile firmato eseguito da un'autorità di timestamp.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URL* \[ di in\]
</dt> <dd>

Stringa che contiene l'URL del server di timestamp.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Un timestamp estende la validità di un certificato verificando che il file eseguibile sia stato firmato al momento del timestamp.

Prima di poter chiamare questo metodo, è necessario specificare il file eseguibile firmato per il timestamp, nella proprietà **SignedCode. FileName** , ed è necessario chiamare il metodo [**SignedCode. Sign**](signedcode-sign.md) per firmare il file eseguibile.

Se il file eseguibile firmato è già contrassegnato come timestamp, questo metodo sovrascrive il timestamp esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
