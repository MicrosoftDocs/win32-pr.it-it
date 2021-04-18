---
description: Contiene la tabella delle informazioni chiave per tutte le interfacce LAN wireless gestite dal servizio di configurazione wireless.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Struttura INTFS_KEY_TABLE (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307835"
---
# <a name="intfs_key_table-structure"></a>Struttura della tabella della \_ chiave INTFS \_

\[**INTFS \_ La \_ tabella delle chiavi** non è più supportata a partire da Windows Vista e windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

La struttura della **\_ \_ tabella della chiave INTFS** contiene la tabella delle informazioni chiave per tutte le interfacce LAN wireless gestite dal servizio di configurazione wireless.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNumIntfs**
</dt> <dd>

Numero totale di interfacce.

</dd> <dt>

**pIntfs**
</dt> <dd>

Puntatore alla struttura [**della \_ \_ voce della chiave INTF**](intf-key-entry.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione *wzcsapi. h* non è disponibile nel Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                       |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




