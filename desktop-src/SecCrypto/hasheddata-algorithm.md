---
description: Imposta o Recupera il tipo di algoritmo di hash utilizzato.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Proprietà HashedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325600"
---
# <a name="hasheddataalgorithm-property"></a>Proprietà HashedData. Algorithm

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La proprietà **Algorithm** imposta o Recupera il tipo di algoritmo hash utilizzato.

## <a name="syntax"></a>Sintassi


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione dell' [**\_ \_ algoritmo hash CAPICOM**](capicom-hash-algorithm.md) che definisce un algoritmo hash. Il valore predefinito è l'algoritmo hash capicol \_ \_ \_ SHA1. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                               | Significato                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <dt>**Algoritmo hash capicot \_ \_ \_ SHA1**</dt> </dl>           | Algoritmo di hash SHA1.<br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <dt>**\_Algoritmo hash CAPICOM \_ \_ MD2**</dt> </dl>              | Algoritmo di hash MD2.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <dt>**\_Algoritmo hash CAPICOM \_ \_ MD4**</dt> </dl>              | Algoritmo di hash MD4.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <dt>**Algoritmo hash capicol \_ \_ \_ MD5**</dt> </dl>              | Algoritmo di hash MD5.<br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <dt>**Algoritmo hash capicol \_ \_ \_ Sha \_ 256**</dt> </dl> | Algoritmo hash SHA-256.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <dt>**Algoritmo hash capicol \_ \_ \_ Sha \_ 384**</dt> </dl> | Algoritmo hash SHA-384.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.<br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <dt>**Algoritmo hash capicol \_ \_ \_ Sha \_ 512**</dt> </dl> | Algoritmo hash SHA-512.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**HashedData**](hasheddata.md)
</dt> </dl>

 

 
