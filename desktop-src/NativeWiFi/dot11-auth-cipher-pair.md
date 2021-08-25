---
description: Definisce una coppia di algoritmi di autenticazione e crittografia 802.11 che possono essere abilitati contemporaneamente nella stazione 802.11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: DOT11_AUTH_CIPHER_PAIR struttura (Wlantypes.h)
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
ms.openlocfilehash: 84e4abde6192cf1be92b21df0c6a79125a198e0fde28e304cf583d76ea91689f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801481"
---
# <a name="dot11_auth_cipher_pair-structure"></a>Struttura DOT11 \_ AUTH \_ CIPHER \_ PAIR

La struttura **DOT11 \_ AUTH \_ CIPHER \_ PAIR** definisce una coppia di algoritmi di autenticazione e crittografia 802.11 che possono essere abilitati contemporaneamente nella stazione 802.11.

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

Algoritmo di autenticazione che usa un [**tipo enumerato \_ DOT11 AUTH \_ ALGORITHM.**](dot11-auth-algorithm.md)

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Algoritmo di crittografia che usa un [**tipo enumerato \_ DOT11 CIPHER \_ ALGORITHM.**](dot11-cipher-algorithm.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura DOT11 AUTH CIPHER PAIR definisce un algoritmo di autenticazione e crittografia che può essere abilitato insieme per le connessioni di rete \_ \_ \_ BSS (Basic Service Set).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                        |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                         |
| Intestazione<br/>                   | <dl> <dt>Wlantypes.h (include Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ALGORITMO DI AUTENTICAZIONE DOT11 \_ \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**ALGORITMO DI CRITTOGRAFIA DOT11 \_ \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




