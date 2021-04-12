---
description: Archivia le informazioni chiave su un'interfaccia LAN wireless gestita dal servizio di configurazione wireless.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Struttura INTF_KEY_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343896"
---
# <a name="intf_key_entry-structure"></a>Struttura della voce della \_ chiave INTF \_

\[**INTF \_ La \_ voce chiave** non è più supportata a partire da Windows Vista e windows Server 2008. Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]

La struttura della **\_ \_ voce della chiave INTF** archivia le informazioni chiave su un'interfaccia LAN wireless gestita dal servizio di configurazione wireless.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**wszGuid**
</dt> <dd>

Puntatore al GUID dell'interfaccia rappresentato come stringa Unicode nel formato seguente: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tabella della chiave INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




