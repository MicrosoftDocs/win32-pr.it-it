---
title: Costanti del gruppo di cache (Wininet.h)
description: L'elenco seguente contiene le costanti utilizzate dalle funzioni del gruppo di cache.
ms.assetid: 9ca2069e-497d-4747-acf4-d5b8020b8ab7
topic_type:
- apiref
api_name:
- CACHEGROUP_ATTRIBUTE_BASIC
- CACHEGROUP_ATTRIBUTE_FLAG
- CACHEGROUP_ATTRIBUTE_GET_ALL
- CACHEGROUP_ATTRIBUTE_GROUPNAME
- CACHEGROUP_ATTRIBUTE_QUOTA
- CACHEGROUP_ATTRIBUTE_STORAGE
- CACHEGROUP_ATTRIBUTE_TYPE
- CACHEGROUP_FLAG_FLUSHURL_ONDELETE
- CACHEGROUP_FLAG_GIDONLY
- CACHEGROUP_FLAG_NONPURGEABLE
- CACHEGROUP_READWRITE_MASK
- CACHEGROUP_SEARCH_ALL
- CACHEGROUP_SEARCH_BYURL
- CACHEGROUP_TYPE_INVALID
- GROUP_OWNER_STORAGE_SIZE
- GROUPNAME_MAX_LENGTH
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb79ae76d743ff4633f6d7f359f96906d2f60cc64c2c35ab2544ae80918721a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955621"
---
# <a name="cache-group-constants"></a>Costanti del gruppo di cache

L'elenco seguente contiene le costanti utilizzate dalle funzioni del gruppo di cache.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**ATTRIBUTO CACHEGROUP \_ \_ BASIC**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Recupera i flag, il tipo e gli attributi di quota del disco del gruppo di cache. Viene usato dalla [**funzione GetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**FLAG DI ATTRIBUTO CACHEGROUP \_ \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Imposta o recupera i flag associati al gruppo di cache. Viene usato dalle [**funzioni GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**ATTRIBUTO CACHEGROUP \_ \_ GET \_ ALL**
</dt> <dd> <dl> <dt>

0xffffffff
</dt> <dt>



Recupera tutti gli attributi del gruppo di cache. Viene usato dalla [**funzione GetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP \_ ATTRIBUTE \_ GROUPNAME**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Imposta o recupera il nome del gruppo di cache. Viene usato dalle [**funzioni GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**QUOTA \_ DELL'ATTRIBUTO \_ CACHEGROUP**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Imposta o recupera la quota del disco associata al gruppo di cache. Viene usato dalle [**funzioni GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**ARCHIVIAZIONE \_ ATTRIBUTI CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Imposta o recupera l'archiviazione proprietaria del gruppo associata al gruppo di cache. Viene usato dalle [**funzioni GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**TIPO DI \_ ATTRIBUTO \_ CACHEGROUP**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Imposta o recupera il tipo di gruppo di cache. Viene usato dalle [**funzioni GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP \_ FLAG \_ FLUSHURL \_ ONDELETE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica che tutte le voci della cache associate al gruppo di cache devono essere eliminate, a meno che la voce non appartenga a un altro gruppo di cache.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP \_ FLAG \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica che la funzione deve creare solo un GROUPID univoco per il gruppo di cache e non il gruppo effettivo.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**FLAG \_ CACHEGROUP \_ NON UTILIZZABILE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica che il gruppo di cache non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP \_ READWRITE \_ MASK**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Imposta il tipo, la quota del disco, il nome del gruppo e gli attributi di archiviazione del proprietario del gruppo di cache. Viene usato dalla [**funzione SetUrlCacheGroupAttribute.**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea)


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**RICERCA DI CACHEGROUP \_ \_ ALL**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica che tutti i gruppi di cache nel sistema dell'utente devono essere enumerati.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP \_ SEARCH \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**TIPO CACHEGROUP \_ \_ NON VALIDO**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica che il tipo di gruppo di cache non è valido.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**DIMENSIONI DI \_ ARCHIVIAZIONE DEL PROPRIETARIO DEL \_ \_ GRUPPO**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Lunghezza dell'array di archiviazione del proprietario del gruppo.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**LUNGHEZZA \_ MASSIMA GROUPNAME \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Numero massimo di caratteri consentiti per il nome di un gruppo di cache.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi del server [usare Microsoft Windows servizi HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



 

