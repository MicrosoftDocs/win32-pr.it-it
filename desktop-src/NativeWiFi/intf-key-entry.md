---
description: Archivia le informazioni chiave su un'interfaccia LAN wireless gestita dal servizio di configurazione wireless.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY struttura (Wzcsapi.h)
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
ms.openlocfilehash: 8d14c65d49d7ed28e2756c2a690cb4a7efa9000417e896a206710bf4365f8cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065151"
---
# <a name="intf_key_entry-structure"></a>Struttura INTF \_ KEY \_ ENTRY

\[**INTF \_ KEY \_ ENTRY** non è più supportato a Windows Vista e Windows Server 2008. Usare invece [l'API Wi-Fi nativa](native-wifi-reference.md), che fornisce funzionalità simili. Per altre informazioni, vedere [Informazioni sull'API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **struttura INTF \_ KEY \_ ENTRY** archivia le informazioni chiave su un'interfaccia LAN wireless gestita dal servizio di configurazione wireless.

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

Puntatore al GUID dell'interfaccia rappresentato come stringa Unicode nel formato seguente: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file *di intestazione Wzcsapi.h* non è disponibile in Windows SDK.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP con SP3<br/>                                                       |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TABELLA DELLE CHIAVI INTFS \_ \_**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




