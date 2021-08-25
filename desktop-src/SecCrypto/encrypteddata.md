---
description: Fornisce proprietà e metodi per crittografare e decrittografare i dati usando una chiave di sessione derivata da un segreto.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Oggetto EncryptedData
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
ms.openlocfilehash: 15a66640ccdf794e88ae9cff04854a40fcfa6b763259da191bcdc6b07f11f449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874491"
---
# <a name="encrypteddata-object"></a>Oggetto EncryptedData

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece Platform Invocation Services (PInvoke) per chiamare le funzioni api Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi. Per informazioni su PInvoke, vedere [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx). Possono essere utili anche .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) parte 1 e .NET e [CryptoAPI tramite P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) parte 2 delle sottosezioni dell'estensione della crittografia .NET con CAPICOM e [P/Invoke.](/previous-versions/ms867087(v=msdn.10))\]

**L'oggetto EncryptedData** fornisce proprietà e metodi per crittografare e decrittografare i dati usando una [*chiave di sessione*](../secgloss/s-gly.md) derivata da un segreto.

> [!Note]  
> CAPICOM non supporta il tipo di contenuto PkcS 7 EncryptedData, ma usa una struttura ASN non standard \# per **EncryptedData.** Pertanto, solo CAPICOM può decrittografare un oggetto CAPICOM **EncryptedData.**

 

## <a name="members"></a>Membri

**L'oggetto EncryptedData** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto EncryptedData** dispone di questi metodi.



| Metodo                                       | Descrizione                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Decrittografare**](encrypteddata-decrypt.md)     | Decrittografa il contenuto crittografato usando il segreto.<br/>                                 |
| [**Crittografare**](encrypteddata-encrypt.md)     | Crittografa il contenuto usando il segreto e l'algoritmo di crittografia correnti.<br/>      |
| [**SetSecret**](encrypteddata-setsecret.md) | Imposta il segreto da cui deriva la chiave della sessione di crittografia/decrittografia.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto EncryptedData** ha queste proprietà.



| Proprietà                                                | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](encrypteddata-algorithm.md)<br/> | Sola lettura<br/>  | Algoritmo usato per la crittografia/decrittografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Contenuto**](encrypteddata-content.md)<br/>     | Lettura/Scrittura<br/> | Contenuto da crittografare o decrittografare. L'impostazione di questa proprietà deve essere eseguita prima [**che venga chiamato**](encrypteddata-encrypt.md) il metodo Encrypt. <br/> Quando il valore di questa proprietà viene reimpostato, [](../secgloss/s-gly.md) direttamente o indirettamente, l'intero stato dell'oggetto viene reimpostato e qualsiasi contenuto crittografato nell'oggetto viene perso.<br/> Questa è la proprietà predefinita.<br/> |



 

## <a name="remarks"></a>Commenti

**L'oggetto EncryptedData** può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto EncryptedData** è CAPICOM. EncryptedData.1.

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
</dt> </dl>

 

 
