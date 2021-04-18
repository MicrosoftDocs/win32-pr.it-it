---
description: Carica un certificato di firma da un file con estensione pfx specificato.
ms.assetid: 98963354-c237-40d0-9235-8318728e2c8e
title: Metodo signer. Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9a817a95ca825b67b54a41fc674db10bf81b5740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330270"
---
# <a name="signerload-method"></a>Metodo signer. Load

\[Il metodo **Load** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Il metodo **Load** carica un certificato di firma da un file con estensione pfx specificato.

## <a name="syntax"></a>Sintassi


```VB
Signer.Load( _
  ByVal FileName, _
  [ ByVal Password ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* 
</dt> <dd>

Nome del file con estensione PFX contenente il certificato di firma.

</dd> <dt>

*Password* \[ di opzionale\]
</dt> <dd>

Stringa contenente la password in testo non crittografato utilizzata per aprire il file. Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione. Il valore predefinito è una stringa vuota (""). Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo carica il primo certificato nel file con estensione pfx a cui è associata una chiave privata.

Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Firmatario**](signer.md)
</dt> </dl>

 

 
