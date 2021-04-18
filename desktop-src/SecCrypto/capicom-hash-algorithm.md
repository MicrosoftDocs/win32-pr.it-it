---
description: L' \_ enumerazione dell'algoritmo hash CAPICOM \_ definisce un algoritmo hash.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Enumerazione CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327645"
---
# <a name="capicom_hash_algorithm-enumeration"></a>\_Enumerazione dell'algoritmo hash \_ capicol

L'enumerazione dell' **\_ \_ algoritmo hash CAPICOM** definisce un algoritmo hash.

## <a name="members"></a>Membri



| Membro                                 | Descrizione                                                                                                                                                                 | Valore |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Algoritmo hash capicot \_ \_ \_ SHA1**     | Sha ( [*Secure Hash Algorithm*](../secgloss/s-gly.md) ) che genera un digest del messaggio a 160 bit.<br/> | 0     |
| **\_Algoritmo hash CAPICOM \_ \_ MD2**      | Algoritmo di hash MD2.<br/>                                                                                                                                           | 1     |
| **\_Algoritmo hash CAPICOM \_ \_ MD4**      | Algoritmo di hash MD4.<br/>                                                                                                                                           | 2     |
| **Algoritmo hash capicol \_ \_ \_ MD5**      | Algoritmo di hash MD5.<br/>                                                                                                                                           | 3     |
| **Algoritmo hash capicol \_ \_ \_ Sha \_ 256** | Algoritmo hash SHA-256.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.<br/>                                                                 | 4     |
| **Algoritmo hash capicol \_ \_ \_ Sha \_ 384** | Algoritmo hash SHA-384.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.<br/>                                                                 | 5     |
| **Algoritmo hash capicol \_ \_ \_ Sha \_ 512** | Algoritmo hash SHA-512.<br/> **CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.<br/>                                                                 | 6     |



## <a name="remarks"></a>Commenti

L'enumerazione dell' **\_ \_ algoritmo hash CAPICOM** viene utilizzata dalla proprietà [**HashedData. Algorithm**](hasheddata-algorithm.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
