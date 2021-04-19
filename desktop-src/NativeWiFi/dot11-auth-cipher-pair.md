---
description: Definisce una coppia di algoritmi di crittografia e autenticazione 802,11 che possono essere abilitati nello stesso momento nella stazione 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Struttura DOT11_AUTH_CIPHER_PAIR (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313767"
---
# <a name="dot11_auth_cipher_pair-structure"></a>\_Struttura delle \_ coppie di crittografia auth DOT11 \_

La struttura delle **\_ \_ \_ coppie di crittografia auth DOT11** definisce una coppia di algoritmi di crittografia e autenticazione 802,11 che possono essere abilitati allo stesso tempo nella stazione 802,11.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Members

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

Algoritmo di autenticazione che usa un tipo enumerato dell' [**\_ \_ algoritmo**](dot11-auth-algorithm.md) di autenticazione DOT11.

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Algoritmo di crittografia che utilizza un tipo enumerato dell' [**\_ \_ algoritmo di crittografia DOT11**](dot11-cipher-algorithm.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

La \_ struttura delle \_ coppie di crittografia auth DOT11 \_ definisce un algoritmo di autenticazione e crittografia che può essere abilitato insieme per le connessioni di rete di base del set di servizi (BSS).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Algoritmo di autenticazione DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**\_Algoritmo di crittografia DOT11 \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




