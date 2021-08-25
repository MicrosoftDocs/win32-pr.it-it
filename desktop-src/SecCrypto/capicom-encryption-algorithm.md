---
description: Definisce gli algoritmi da usare nella crittografia e nella decrittografia.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: CAPICOM_ENCRYPTION_ALGORITHM enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d0f66c1e8ec59819f4f01c5f46989e1f904930f3699f978b26c6ab7c5107154c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879341"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>Enumerazione CAPICOM \_ ENCRYPTION \_ ALGORITHM

Il **tipo di enumerazione CAPICOM ENCRYPTION \_ \_ ALGORITHM** definisce gli algoritmi da usare nella crittografia e nella decrittografia.

## <a name="members"></a>Membri



| Membro                                   | Descrizione                                                                                                                                                                                              | Valore     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **ALGORITMO DI CRITTOGRAFIA CAPICOM \_ \_ \_ RC2**  | Usare la crittografia RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **ALGORITMO DI CRITTOGRAFIA CAPICOM \_ \_ \_ RC4**  | Usare la crittografia RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **ALGORITMO DI CRITTOGRAFIA CAPICOM \_ \_ \_ DES**  | Usare la crittografia DES.<br/>                                                                                                                                                                           | 2         |
| **ALGORITMO DI CRITTOGRAFIA CAPICOM \_ \_ \_ 3DES** | Usare la crittografia DES tripla.<br/>                                                                                                                                                                    | 3         |
| **AES \_ \_ DELL'ALGORITMO \_ DI CRITTOGRAFIA CAPICOM**  | Usare [*l'algoritmo*](../secgloss/a-gly.md) Advanced Encryption Standard (AES). Questo valore è valido solo per [**l'oggetto EncryptedData.**](encrypteddata.md)<br/> | 4 // v2.0 |



## <a name="remarks"></a>Commenti

Il **tipo di enumerazione CAPICOM ENCRYPTION \_ \_ ALGORITHM** viene usato dalla [**proprietà Algorithm.Name.**](algorithm-name.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
