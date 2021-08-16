---
description: Decrittografa una stringa di dati crittografata e codificata.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Metodo EncryptedData.Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8bf8a108efdc462a9f08a508a05b736817ec38ce43ee50dbd3fdd11aa2af9f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766697"
---
# <a name="encrypteddatadecrypt-method"></a>Metodo EncryptedData.Decrypt

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni api Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi. Per informazioni su PInvoke, vedere [Esercitazione su Platform Invoke.](https://msdn.microsoft.com/library/aa288468.aspx) Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

Il **metodo Decrypt** decrittografa una stringa di dati crittografata e codificata. I dati di testo non crittografato risultanti diventano [**la proprietà Content**](encrypteddata-content.md) [**dell'oggetto EncryptedData.**](encrypteddata.md) La decrittografia del contenuto ha esito negativo a meno che il segreto, impostato dal [**metodo SetSecret,**](encrypteddata-setsecret.md) non corrisponda esattamente al segreto usato per derivare la chiave usata per crittografare il contenuto.

## <a name="syntax"></a>Sintassi


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncryptedMessage* \[ Pollici\]
</dt> <dd>

Stringa contenente i dati codificati e crittografati da decrittografare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiave di sessione derivata dal segreto corrente viene usata per la decrittografia. Questo metodo non produrrà il testo non crittografato corretto a meno che il segreto corrente non corrisponda esattamente al segreto usato per crittografare il messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**Encrypteddata**](encrypteddata.md)
</dt> </dl>

 

 
