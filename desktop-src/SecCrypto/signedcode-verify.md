---
description: Verifica la firma Authenticode nel codice firmato.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: Metodo SignedCode.Verify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff9f726b0ce05a3e6c03808b8676a229737a9924a7195c4a9a6841b38f025959
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974029"
---
# <a name="signedcodeverify-method"></a>Metodo SignedCode.Verify

\[Il **metodo** Verify è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)e [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) dell'API Win32 per firmare il contenuto con una firma digitale Authenticode. Per informazioni su PInvoke, vedere [Esercitazione su Platform Invoke.](https://msdn.microsoft.com/library/aa288468.aspx) Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

Il **metodo Verify** verifica la firma Authenticode nel codice firmato.

## <a name="syntax"></a>Sintassi


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bUIAllowed* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che specifica se viene utilizzata una finestra di dialogo per verificare la firma. Se true, viene generata una finestra di dialogo per determinare se il codice è attendibile. Il valore predefinito è false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SignedCode**](signedcode.md)
</dt> </dl>

 

 
