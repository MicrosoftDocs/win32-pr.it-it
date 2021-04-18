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
# <a name="cache-group-constants"></a><span data-ttu-id="66585-103">Costanti gruppo cache</span><span class="sxs-lookup"><span data-stu-id="66585-103">Cache Group Constants</span></span>

<span data-ttu-id="66585-104">Nell'elenco seguente sono contenute le costanti utilizzate dalle funzioni del gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-104">The following list contains the constants used by the cache group functions.</span></span>

<dl> <dt>

<span data-ttu-id="66585-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**\_attributo CACHEGROUP \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="66585-105"><span id="CACHEGROUP_ATTRIBUTE_BASIC"></span><span id="cachegroup_attribute_basic"></span>**CACHEGROUP\_ATTRIBUTE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="66585-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="66585-107">Recupera i flag, il tipo e gli attributi della quota del disco del gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-107">Retrieves the flags, type, and disk quota attributes of the cache group.</span></span> <span data-ttu-id="66585-108">Viene usato dalla funzione [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-108">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**\_flag dell'attributo CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="66585-109"><span id="CACHEGROUP_ATTRIBUTE_FLAG"></span><span id="cachegroup_attribute_flag"></span>**CACHEGROUP\_ATTRIBUTE\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="66585-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="66585-111">Imposta o recupera i flag associati al gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-111">Sets or retrieves the flags associated with the cache group.</span></span> <span data-ttu-id="66585-112">Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-112">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**\_attributo CACHEGROUP \_ get \_ All**</span><span class="sxs-lookup"><span data-stu-id="66585-113"><span id="CACHEGROUP_ATTRIBUTE_GET_ALL"></span><span id="cachegroup_attribute_get_all"></span>**CACHEGROUP\_ATTRIBUTE\_GET\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-114">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="66585-114">0xffffffff</span></span>
</dt> <dt>



<span data-ttu-id="66585-115">Recupera tutti gli attributi del gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-115">Retrieves all the attributes of the cache group.</span></span> <span data-ttu-id="66585-116">Viene usato dalla funzione [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-116">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**\_ \_ GroupName attributo CACHEGROUP**</span><span class="sxs-lookup"><span data-stu-id="66585-117"><span id="CACHEGROUP_ATTRIBUTE_GROUPNAME"></span><span id="cachegroup_attribute_groupname"></span>**CACHEGROUP\_ATTRIBUTE\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-118">0x000000010</span><span class="sxs-lookup"><span data-stu-id="66585-118">0x000000010</span></span>
</dt> <dt>



<span data-ttu-id="66585-119">Imposta o Recupera il nome del gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-119">Sets or retrieves the group name of the cache group.</span></span> <span data-ttu-id="66585-120">Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-120">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**\_quota dell'attributo CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="66585-121"><span id="CACHEGROUP_ATTRIBUTE_QUOTA"></span><span id="cachegroup_attribute_quota"></span>**CACHEGROUP\_ATTRIBUTE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="66585-122">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="66585-123">Imposta o recupera la quota disco associata al gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-123">Sets or retrieves the disk quota associated with the cache group.</span></span> <span data-ttu-id="66585-124">Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-124">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**\_archiviazione degli attributi di CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="66585-125"><span id="CACHEGROUP_ATTRIBUTE_STORAGE"></span><span id="cachegroup_attribute_storage"></span>**CACHEGROUP\_ATTRIBUTE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="66585-126">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="66585-127">Imposta o recupera lo spazio di archiviazione del proprietario del gruppo associato al gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-127">Sets or retrieves the group owner storage associated with the cache group.</span></span> <span data-ttu-id="66585-128">Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-128">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**\_tipo di attributo CACHEGROUP \_**</span><span class="sxs-lookup"><span data-stu-id="66585-129"><span id="CACHEGROUP_ATTRIBUTE_TYPE"></span><span id="cachegroup_attribute_type"></span>**CACHEGROUP\_ATTRIBUTE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="66585-130">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="66585-131">Imposta o Recupera il tipo di gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-131">Sets or retrieves the cache group type.</span></span> <span data-ttu-id="66585-132">Viene usato dalle funzioni [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) e [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-132">This is used by the [**GetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-geturlcachegroupattributea) and [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**\_flag CACHEGROUP \_ FLUSHURL \_ OnDelete**</span><span class="sxs-lookup"><span data-stu-id="66585-133"><span id="CACHEGROUP_FLAG_FLUSHURL_ONDELETE"></span><span id="cachegroup_flag_flushurl_ondelete"></span>**CACHEGROUP\_FLAG\_FLUSHURL\_ONDELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="66585-134">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="66585-135">Indica che tutte le voci della cache associate al gruppo di cache devono essere eliminate, a meno che la voce appartenga a un altro gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-135">Indicates that all the cache entries associated with the cache group should be deleted, unless the entry belongs to another cache group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**\_flag CACHEGROUP \_ GIDONLY**</span><span class="sxs-lookup"><span data-stu-id="66585-136"><span id="CACHEGROUP_FLAG_GIDONLY"></span><span id="cachegroup_flag_gidonly"></span>**CACHEGROUP\_FLAG\_GIDONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="66585-137">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="66585-138">Indica che la funzione deve creare solo un GROUPID univoco per il gruppo di cache e non creare il gruppo effettivo.</span><span class="sxs-lookup"><span data-stu-id="66585-138">Indicates that the function should only create a unique GROUPID for the cache group and not create the actual group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**\_flag CACHEGROUP \_ NONPURGEABLE**</span><span class="sxs-lookup"><span data-stu-id="66585-139"><span id="CACHEGROUP_FLAG_NONPURGEABLE"></span><span id="cachegroup_flag_nonpurgeable"></span>**CACHEGROUP\_FLAG\_NONPURGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-140">0x00000001</span><span class="sxs-lookup"><span data-stu-id="66585-140">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="66585-141">Indica che il gruppo di cache non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="66585-141">Indicates that the cache group cannot be purged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**\_maschera CACHEGROUP ReadWrite \_**</span><span class="sxs-lookup"><span data-stu-id="66585-142"><span id="CACHEGROUP_READWRITE_MASK"></span><span id="cachegroup_readwrite_mask"></span>**CACHEGROUP\_READWRITE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-143">0x0000003c</span><span class="sxs-lookup"><span data-stu-id="66585-143">0x0000003c</span></span>
</dt> <dt>



<span data-ttu-id="66585-144">Imposta il tipo, la quota del disco, il nome del gruppo e gli attributi di archiviazione del proprietario del gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-144">Sets the type, disk quota, group name, and owner storage attributes of the cache group.</span></span> <span data-ttu-id="66585-145">Viene usato dalla funzione [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) .</span><span class="sxs-lookup"><span data-stu-id="66585-145">This is used by the [**SetUrlCacheGroupAttribute**](/windows/desktop/api/Wininet/nf-wininet-seturlcachegroupattributea) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP \_ Cerca \_ tutto**</span><span class="sxs-lookup"><span data-stu-id="66585-146"><span id="CACHEGROUP_SEARCH_ALL"></span><span id="cachegroup_search_all"></span>**CACHEGROUP\_SEARCH\_ALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66585-147">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="66585-148">Indica che tutti i gruppi di cache nel sistema dell'utente devono essere enumerati.</span><span class="sxs-lookup"><span data-stu-id="66585-148">Indicates that all of the cache groups in the user's system should be enumerated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**\_ricerca CACHEGROUP \_ BYURL**</span><span class="sxs-lookup"><span data-stu-id="66585-149"><span id="CACHEGROUP_SEARCH_BYURL"></span><span id="cachegroup_search_byurl"></span>**CACHEGROUP\_SEARCH\_BYURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-150">0x00000001</span><span class="sxs-lookup"><span data-stu-id="66585-150">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="66585-151">Non implementato attualmente.</span><span class="sxs-lookup"><span data-stu-id="66585-151">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**tipo di CACHEGROUP \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="66585-152"><span id="CACHEGROUP_TYPE_INVALID"></span><span id="cachegroup_type_invalid"></span>**CACHEGROUP\_TYPE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="66585-153">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="66585-154">Indica che il tipo di gruppo di cache non è valido.</span><span class="sxs-lookup"><span data-stu-id="66585-154">Indicates that the cache group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**\_dimensioni di \_ archiviazione del proprietario del gruppo \_**</span><span class="sxs-lookup"><span data-stu-id="66585-155"><span id="GROUP_OWNER_STORAGE_SIZE"></span><span id="group_owner_storage_size"></span>**GROUP\_OWNER\_STORAGE\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-156">0x00000004</span><span class="sxs-lookup"><span data-stu-id="66585-156">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="66585-157">Lunghezza dell'array di archiviazione del proprietario del gruppo.</span><span class="sxs-lookup"><span data-stu-id="66585-157">Length of the group owner storage array.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="66585-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**\_lunghezza massima GroupName \_**</span><span class="sxs-lookup"><span data-stu-id="66585-158"><span id="GROUPNAME_MAX_LENGTH"></span><span id="groupname_max_length"></span>**GROUPNAME\_MAX\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66585-159">0x00000078</span><span class="sxs-lookup"><span data-stu-id="66585-159">0x00000078</span></span>
</dt> <dt>



<span data-ttu-id="66585-160">Numero massimo di caratteri consentiti per il nome di un gruppo di cache.</span><span class="sxs-lookup"><span data-stu-id="66585-160">Maximum number of characters allowed for a cache group name.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66585-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="66585-161">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="66585-162">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="66585-162">WinINet does not support server implementations.</span></span> <span data-ttu-id="66585-163">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="66585-163">In addition, it should not be used from a service.</span></span> <span data-ttu-id="66585-164">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="66585-164">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66585-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66585-165">Requirements</span></span>



| <span data-ttu-id="66585-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="66585-166">Requirement</span></span> | <span data-ttu-id="66585-167">Valore</span><span class="sxs-lookup"><span data-stu-id="66585-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66585-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66585-168">Minimum supported client</span></span><br/> | <span data-ttu-id="66585-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66585-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="66585-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66585-170">Minimum supported server</span></span><br/> | <span data-ttu-id="66585-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66585-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="66585-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66585-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="66585-173"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="66585-173"><dt>Wininet.h</dt></span></span> </dl> |



 

