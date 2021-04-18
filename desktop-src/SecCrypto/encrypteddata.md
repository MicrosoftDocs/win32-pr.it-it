---
description: Fornisce proprietà e metodi per crittografare e decrittografare i dati usando una chiave di sessione derivata da un segreto.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: EncryptedData (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324896"
---
# <a name="encrypteddata-object"></a>EncryptedData (oggetto)

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi. Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx). Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

L'oggetto **EncryptedData** fornisce proprietà e metodi per crittografare e decrittografare i dati usando una [*chiave di sessione*](../secgloss/s-gly.md) derivata da un segreto.

> [!Note]  
> CAPICOM non supporta il \# tipo di contenuto EncryptedData di PKCS 7, ma usa una struttura ASN non standard per **EncryptedData**. Pertanto, solo CAPICOM è in grado di decrittografare un oggetto capicot **EncryptedData** .

 

## <a name="members"></a>Membri

L'oggetto **EncryptedData** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **EncryptedData** ha questi metodi.



| Metodo                                       | Descrizione                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Decrypt**](encrypteddata-decrypt.md)     | Decrittografa il contenuto crittografato usando il segreto.<br/>                                 |
| [**Crittografare**](encrypteddata-encrypt.md)     | Crittografa il contenuto utilizzando l'algoritmo di crittografia e il segreto corrente.<br/>      |
| [**Sesecret**](encrypteddata-setsecret.md) | Imposta il segreto da cui viene derivata la chiave della sessione di crittografia/decrittografia.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **EncryptedData** dispone di queste proprietà.



| Proprietà                                                | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](encrypteddata-algorithm.md)<br/> | Sola lettura<br/>  | Algoritmo utilizzato per la crittografia/decrittografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Contenuto**](encrypteddata-content.md)<br/>     | Lettura/Scrittura<br/> | Contenuto da crittografare o decrittografare. L'impostazione di questa proprietà deve essere eseguita prima che venga chiamato il metodo [**Encrypt**](encrypteddata-encrypt.md) . <br/> Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e qualsiasi contenuto crittografato nell'oggetto viene perso.<br/> Si tratta della proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile creare l'oggetto **EncryptedData** ed è sicuro per lo scripting. Il ProgID per l'oggetto **EncryptedData** è capicom. EncryptedData. 1.

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
</dt> </dl>

 

 
