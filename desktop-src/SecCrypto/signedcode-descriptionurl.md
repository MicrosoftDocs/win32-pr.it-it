---
description: Imposta o recupera l'URL di una descrizione del file eseguibile firmato.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Proprietà SignedCode.DescriptionURL
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
ms.openlocfilehash: 2668be4a9b0d4c6d746d0849c884c9819ad0d9291049e806e73fc1cea1b49d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974208"
---
# <a name="signedcodedescriptionurl-property"></a>Proprietà SignedCode.DescriptionURL

\[La **proprietà DescriptionURL** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere [Esercitazione su Platform Invoke.](https://msdn.microsoft.com/library/aa288468.aspx) Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

La **proprietà DescriptionURL** imposta o recupera l'URL di una descrizione del file eseguibile firmato.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Valore proprietà

URL di una descrizione del file eseguibile firmato.

## <a name="remarks"></a>Commenti

**DescriptionURL è** l'URL a cui [**si**](signedcode-description.md) collega la descrizione visualizzata nella finestra di dialogo di verifica Authenticode. Se questa proprietà è **NULL,** la **descrizione** non funziona come collegamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
