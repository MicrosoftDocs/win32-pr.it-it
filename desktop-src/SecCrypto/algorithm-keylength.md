---
description: Imposta o recupera la lunghezza della chiave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Proprietà Algorithm.KeyLength
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
ms.openlocfilehash: c5ce8f906628df06ef506a0f57c33db4bed7c5980bb78ab2e0094d0443b5646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773665"
---
# <a name="algorithmkeylength-property"></a>Proprietà Algorithm.KeyLength

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **proprietà KeyLength** imposta o recupera la lunghezza della chiave.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a>Valore proprietà

Valore [**dell'enumerazione CAPICOM \_ ENCRYPTION KEY \_ \_ LENGTH**](capicom-encryption-key-length.md) che specifica la lunghezza della chiave. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                        | Significato                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <dt>**LUNGHEZZA MASSIMA \_ DELLA CHIAVE DI CRITTOGRAFIA \_ \_ \_ CAPICOM**</dt> </dl>     | Usare la lunghezza massima della chiave disponibile con l'algoritmo di crittografia indicato.<br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <dt>**LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 40 \_ BIT**</dt> </dl>    | Usare chiavi a 40 bit.<br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <dt>**LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 56 \_ BIT**</dt> </dl>    | Usare chiavi a 56 bit, se disponibili.<br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <dt>**LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 128 \_ BIT**</dt> </dl> | Usare chiavi a 128 bit, se disponibili.<br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <dt>**LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 192 \_ BIT**</dt> </dl> | Usare chiavi a 192 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <dt>**LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 256 \_ BIT**</dt> </dl> | Usare chiavi a 256 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  |



 

## <a name="remarks"></a>Commenti

Quando vengono usati algoritmi di crittografia DES e 3DES, le lunghezze delle chiavi sono standard e la **proprietà KeyLength** viene ignorata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Algoritmo**](algorithm.md)
</dt> </dl>

 

 
