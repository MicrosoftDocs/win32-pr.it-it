---
description: Definisce la lunghezza della chiave da utilizzare nella crittografia.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Enumerazione CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
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
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333568"
---
# <a name="capicom_encryption_key_length-enumeration"></a>\_Enumerazione della lunghezza della chiave di crittografia CAPICOM \_ \_

Il tipo di enumerazione della **lunghezza della \_ chiave di crittografia \_ \_ CAPICOM** definisce la [*lunghezza della chiave*](../secgloss/k-gly.md) da usare nella crittografia.

## <a name="members"></a>Membri



| Membro                                          | Descrizione                                                                               | Valore     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| **\_lunghezza della chiave di crittografia CAPICOM \_ \_ \_ massima**   | Usa la lunghezza massima della chiave disponibile con l'algoritmo di crittografia indicato.<br/> | 0         |
| **\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 40 \_ bit**  | USA chiavi a 40 bit.<br/>                                                              | 1         |
| **\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 56 \_ bit**  | USA chiavi a 56 bit se disponibili.<br/>                                                 | 2         |
| **\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 128 \_ bit** | USA chiavi a 128 bit se disponibili.<br/>                                                | 3         |
| **\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 192 \_ bit** | USA chiavi a 192 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  | 4//v 2.0 |
| **\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 256 \_ bit** | USA chiavi a 256 bit. Questa lunghezza della chiave è disponibile solo per AES.<br/>                  | 5//v 2.0 |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione della lunghezza della chiave di crittografia CAPICOM viene usato dalla proprietà [**Algorithm.**](algorithm-keylength.md) **\_ \_ Key \_** length.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
