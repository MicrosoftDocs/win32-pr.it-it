---
description: Imposta o recupera la lunghezza della chiave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Proprietà Algorithm. FileLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324599"
---
# <a name="algorithmkeylength-property"></a>Proprietà Algorithm. FileLength

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà della **lunghezza** della chiave imposta o recupera la lunghezza della chiave.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione di [**\_ \_ \_ lunghezza della chiave di crittografia CAPICOM**](capicom-encryption-key-length.md) che specifica la lunghezza della chiave. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                        | Significato                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**\_lunghezza della chiave di crittografia CAPICOM \_ \_ \_ massima**</dt> </dl>     | Utilizzare la lunghezza massima della chiave disponibile con l'algoritmo di crittografia indicato.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 40 \_ bit**</dt> </dl>    | Usare chiavi a 40 bit.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 56 \_ bit**</dt> </dl>    | Se disponibili, utilizzare chiavi a 56 bit.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 128 \_ bit**</dt> </dl> | Se disponibili, utilizzare chiavi a 128 bit.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 192 \_ bit**</dt> </dl> | Usare chiavi a 192 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 256 \_ bit**</dt> </dl> | Usare chiavi a 256 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  |



 

## <a name="remarks"></a>Commenti

Quando si utilizzano gli algoritmi di crittografia DES e 3DES, le lunghezze delle chiavi sono standard e la proprietà della **lunghezza** della chiave viene ignorata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Algoritmo**](algorithm.md)
</dt> </dl>

 

 
