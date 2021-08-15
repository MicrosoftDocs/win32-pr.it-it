---
description: La proprietà FileName imposta o recupera il percorso del file eseguibile. Si tratta della proprietà predefinita.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Proprietà SignedCode.FileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 981ff6e1343f836ef145d1dac8c66b93d7a89c885a04cb2fe024740d7e35a53d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900381"
---
# <a name="signedcodefilename-property"></a>Proprietà SignedCode.FileName

\[La **proprietà FileName** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

La **proprietà FileName** imposta o recupera il percorso del file eseguibile. Si tratta della proprietà predefinita.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>Valore proprietà

Percorso del file eseguibile.

## <a name="remarks"></a>Commenti

Se il valore della **proprietà FileName** viene modificato, lo stato dell'intero [**oggetto SignedCode**](signedcode.md) viene reimpostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
