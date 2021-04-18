---
title: Costanti di gruppo della cache (WinInet. h)
description: Nell'elenco seguente sono contenute le costanti utilizzate dalle funzioni del gruppo di cache.
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
ms.openlocfilehash: 3a08efa37ad78fa3351d12fa43491c7b62ee64af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302332"
---
# <a name="cache-group-constants"></a>Costanti gruppo cache

Nell'elenco seguente sono contenute le costanti utilizzate dalle funzioni del gruppo di cache.

<dl> <dt>

<span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_attributo CACHEGROUP \_ Basic**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Recupera i flag, il tipo e gli attributi della quota del disco del gruppo di cache. Viene usato dalla funzione [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_flag dell'attributo CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Imposta o recupera i flag associati al gruppo di cache. Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_attributo CACHEGROUP \_ get \_ All**
</dt> <dd> <dl> <dt>

0xFFFFFFFF
</dt> <dt>



Recupera tutti gli attributi del gruppo di cache. Viene usato dalla funzione [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_ \_ GroupName attributo CACHEGROUP**
</dt> <dd> <dl> <dt>

0x000000010
</dt> <dt>



Imposta o Recupera il nome del gruppo di cache. Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_quota dell'attributo CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Imposta o recupera la quota disco associata al gruppo di cache. Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_archiviazione degli attributi di CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Imposta o recupera lo spazio di archiviazione del proprietario del gruppo associato al gruppo di cache. Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_tipo di attributo CACHEGROUP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Imposta o Recupera il tipo di gruppo di cache. Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**\_flag CACHEGROUP \_ FLUSHURL \_ OnDelete**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indica che tutte le voci della cache associate al gruppo di cache devono essere eliminate, a meno che la voce appartenga a un altro gruppo di cache.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_flag CACHEGROUP \_ GIDONLY**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indica che la funzione deve creare solo un GROUPID univoco per il gruppo di cache e non creare il gruppo effettivo.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**\_flag CACHEGROUP \_ NONPURGEABLE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica che il gruppo di cache non può essere eliminato.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_maschera CACHEGROUP ReadWrite \_**
</dt> <dd> <dl> <dt>

0x0000003c
</dt> <dt>



Imposta il tipo, la quota del disco, il nome del gruppo e gli attributi di archiviazione del proprietario del gruppo di cache. Viene usato dalla funzione [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ Cerca \_ tutto**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indica che tutti i gruppi di cache nel sistema dell'utente devono essere enumerati.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**\_ricerca CACHEGROUP \_ BYURL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Non implementato attualmente.


</dt> </dl> </dd> <dt>

<span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**tipo di CACHEGROUP \_ \_ non valido**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indica che il tipo di gruppo di cache non è valido.


</dt> </dl> </dd> <dt>

<span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_dimensioni di \_ archiviazione del proprietario del gruppo \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Lunghezza dell'array di archiviazione del proprietario del gruppo.


</dt> </dl> </dd> <dt>

<span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_lunghezza massima GroupName \_**
</dt> <dd> <dl> <dt>

0x00000078
</dt> <dt>



Numero massimo di caratteri consentiti per il nome di un gruppo di cache.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>WinInet. h</dt> </dl> |



 

