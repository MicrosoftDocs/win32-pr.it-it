---
description: Imposta o recupera la descrizione del file eseguibile firmato.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Proprietà SignedCode.Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6046beae61aebaf33ea5eedb6ef2ec643f2edb39dbbedc61372085be2220068b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900351"
---
# <a name="signedcodedescription-property"></a>Proprietà SignedCode.Description

\[La **proprietà** Description è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

La **proprietà Description** imposta o recupera la descrizione del file eseguibile firmato.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.Description As String
```



## <a name="property-value"></a>Valore proprietà

Descrizione del file eseguibile firmato.

## <a name="remarks"></a>Commenti

La descrizione è il testo visualizzato nella finestra di dialogo di verifica Authenticode. Il testo deve descrivere il file eseguibile firmato. Se questa proprietà è **NULL,** nella finestra di dialogo viene visualizzato il nome del file eseguibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
