---
description: Imposta o recupera l'URL di una descrizione del file eseguibile firmato.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Proprietà SignedCode. DescriptionURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325460"
---
# <a name="signedcodedescriptionurl-property"></a>Proprietà SignedCode. DescriptionURL

\[La proprietà **DescriptionURL** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

La proprietà **DescriptionURL** imposta o recupera l'URL di una descrizione del file eseguibile firmato.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Valore proprietà

URL di una descrizione del file eseguibile firmato.

## <a name="remarks"></a>Commenti

**DescriptionURL** è l'URL a cui è collegata la [**Descrizione**](signedcode-description.md) visualizzata nella finestra di dialogo di verifica Authenticode. Se questa proprietà è **null**, la **Descrizione** non funzionerà come collegamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
