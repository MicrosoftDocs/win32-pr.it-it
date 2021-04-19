---
description: Definisce gli algoritmi da utilizzare per la crittografia e la decrittografia.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Enumerazione CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
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
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328138"
---
# <a name="capicom_encryption_algorithm-enumeration"></a>\_Enumerazione dell'algoritmo di crittografia CAPICOM \_

Il tipo di enumerazione di **\_ \_ algoritmi di crittografia CAPICOM** definisce gli algoritmi da utilizzare per la crittografia e la decrittografia.

## <a name="members"></a>Membri



| Membro                                   | Descrizione                                                                                                                                                                                              | Valore     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| **Algoritmo di crittografia capicol \_ \_ \_ RC2**  | Usare la crittografia RSA RC2.<br/>                                                                                                                                                                       | 0         |
| **\_Algoritmo di crittografia CAPICOM \_ \_ RC4**  | Usare la crittografia RSA RC4.<br/>                                                                                                                                                                       | 1         |
| **\_algoritmo di crittografia CAPICOM \_ \_ des**  | Usare la crittografia DES.<br/>                                                                                                                                                                           | 2         |
| **Algoritmo di crittografia capicol \_ \_ \_ 3DES** | Usare la crittografia Triple DES.<br/>                                                                                                                                                                    | 3         |
| **algoritmo di crittografia capicol \_ \_ \_ AES**  | Usare l'algoritmo [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES). Questo valore è valido solo per l'oggetto [**EncryptedData**](encrypteddata.md) .<br/> | 4//v 2.0 |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione dell' **\_ \_ algoritmo di crittografia CAPICOM** viene usato dalla proprietà [**Algorithm.Name**](algorithm-name.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
