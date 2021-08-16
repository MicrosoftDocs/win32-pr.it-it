---
description: Definisce la lunghezza della chiave da usare nella crittografia.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: CAPICOM_ENCRYPTION_KEY_LENGTH enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2957bd644fdf405fec7e82a487bf83af2cbae35ae305f10b9b168628a30b0749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772476"
---
# <a name="capicom_encryption_key_length-enumeration"></a>Enumerazione CAPICOM \_ ENCRYPTION \_ KEY \_ LENGTH

Il **tipo di enumerazione CAPICOM ENCRYPTION KEY \_ \_ \_ LENGTH** definisce la [*lunghezza della*](../secgloss/k-gly.md) chiave da usare nella crittografia.

## <a name="members"></a>Membri



| Membro                                          | Descrizione                                                                               | Valore     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **LUNGHEZZA MASSIMA \_ DELLA CHIAVE DI CRITTOGRAFIA \_ \_ \_ CAPICOM**   | Usa la lunghezza massima della chiave disponibile con l'algoritmo di crittografia indicato.<br/> | 0         |
| **LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 40 \_ BIT**  | Usa chiavi a 40 bit.<br/>                                                              | 1         |
| **LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 56 \_ BIT**  | Usa chiavi a 56 bit, se disponibili.<br/>                                                 | 2         |
| **LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 128 \_ BIT** | Usa chiavi a 128 bit, se disponibili.<br/>                                                | 3         |
| **LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 192 \_ BIT** | Usa chiavi a 192 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  | 4 // v2.0 |
| **LUNGHEZZA CHIAVE DI CRITTOGRAFIA CAPICOM \_ \_ \_ \_ 256 \_ BIT** | Usa chiavi a 256 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  | 5 // v2.0 |



## <a name="remarks"></a>Commenti

Il **tipo di enumerazione CAPICOM ENCRYPTION KEY \_ \_ \_ LENGTH** viene usato dalla [**proprietà Algorithm.KeyLength.**](algorithm-keylength.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
