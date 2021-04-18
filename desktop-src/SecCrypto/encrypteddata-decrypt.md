---
description: Decrittografa una stringa di dati crittografata e codificata.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Metodo EncryptedData. Decrypt
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
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324901"
---
# <a name="encrypteddatadecrypt-method"></a>Metodo EncryptedData. Decrypt

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

Il metodo **Decrypt** decrittografa una stringa di dati crittografata e codificata. I dati in testo non crittografato risultanti diventano la proprietà [**Content**](encrypteddata-content.md) dell'oggetto [**EncryptedData**](encrypteddata.md) . La decrittografia del contenuto ha esito negativo a meno che il segreto, impostato dal metodo [**sesecret**](encrypteddata-setsecret.md) , corrisponda esattamente a quello del segreto usato per derivare la chiave usata per crittografare il contenuto.

## <a name="syntax"></a>Sintassi


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*EncryptedMessage* \[ in\]
</dt> <dd>

Stringa che contiene i dati crittografati codificati da decrittografare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiave della sessione derivata dal segreto corrente viene usata per la decrittografia. Questo metodo non produrrà il testo non crittografato corretto, a meno che il segreto corrente corrisponda esattamente al segreto usato per crittografare il messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
