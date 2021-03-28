---
description: Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel registro di sistema.
title: REGSAM (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983086"
---
# <a name="regsam"></a><span data-ttu-id="ee8d8-103">REGSAM</span><span class="sxs-lookup"><span data-stu-id="ee8d8-103">REGSAM</span></span>

<span data-ttu-id="ee8d8-104">Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-104">A data type used for specifying the security access attributes in the registry.</span></span>



| <span data-ttu-id="ee8d8-105">Costante</span><span class="sxs-lookup"><span data-stu-id="ee8d8-105">Constant</span></span>                                                                                                                                                                                   | <span data-ttu-id="ee8d8-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee8d8-106">Description</span></span>                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <span data-ttu-id="ee8d8-107"><dt>**CHIAVE \_ tutti gli \_ accessi**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-107"><dt>**KEY\_ALL\_ACCESS**</dt></span></span> </dl>                          | <span data-ttu-id="ee8d8-108">Combinazione di \* \* \* \* \_ valore query chiave \_ \* \* \* \*, \* \* \* \* chiave \_ enumerazione \_ \_ sottochiavi \* \* \* \*, \* \* \* \* notifica chiave \* \* \* \* \_ , \* \* \* \* chiave \_ creazione della chiave \_ secondaria \* \* \* \* \_ , \* \* \* \* chiave \_ creazione \_ collegamento \* \* \* \* e \* \_ \_ \* \* \* \* \* \* \* \* \* \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ee8d8-108">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, \*\*\*\*KEY\_NOTIFY\*\*\*\*, \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\*, \*\*\*\*KEY\_CREATE\_LINK\*\*\*\*, and \*\*\*\*KEY\_SET\_VALUE\*\*\*\* access.</span></span><br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <span data-ttu-id="ee8d8-109"><dt>**\_collegamento creazione \_ chiave**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-109"><dt>**KEY\_CREATE\_LINK**</dt></span></span> </dl>                       | <span data-ttu-id="ee8d8-110">Autorizzazione per creare un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-110">Permission to create a symbolic link.</span></span><br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <span data-ttu-id="ee8d8-111"><dt>**CHIAVE \_ creazione chiave \_ secondaria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-111"><dt>**KEY\_CREATE\_SUB\_KEY**</dt></span></span> </dl>             | <span data-ttu-id="ee8d8-112">Autorizzazione per la creazione di sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-112">Permission to create subkeys.</span></span><br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <span data-ttu-id="ee8d8-113"><dt>**CHIAVE \_ enumerazione \_ \_ sottochiavi**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-113"><dt>**KEY\_ENUMERATE\_SUB\_KEYS**</dt></span></span> </dl> | <span data-ttu-id="ee8d8-114">Autorizzazione per enumerare le sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-114">Permission to enumerate subkeys.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <span data-ttu-id="ee8d8-115"><dt>**esecuzione della chiave \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-115"><dt>**KEY\_EXECUTE**</dt></span></span> </dl>                                    | <span data-ttu-id="ee8d8-116">Autorizzazione per l'accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-116">Permission for read access.</span></span><br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <span data-ttu-id="ee8d8-117"><dt>**\_notifica chiave**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-117"><dt>**KEY\_NOTIFY**</dt></span></span> </dl>                                       | <span data-ttu-id="ee8d8-118">Autorizzazione per la notifica di modifica.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-118">Permission for change notification.</span></span><br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <span data-ttu-id="ee8d8-119"><dt>**\_valore query \_ chiave**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-119"><dt>**KEY\_QUERY\_VALUE**</dt></span></span> </dl>                       | <span data-ttu-id="ee8d8-120">Autorizzazione per eseguire query sui dati della sottochiave.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-120">Permission to query subkey data.</span></span><br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <span data-ttu-id="ee8d8-121"><dt>**\_lettura chiave**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-121"><dt>**KEY\_READ**</dt></span></span> </dl>                                             | <span data-ttu-id="ee8d8-122">Combinazione di \* \* \* \* \_ valore di query chiave \_ \* \* \* \*, \* \* \* \* \_ enumerazione \_ chiavi \_ sottochiavi \* \* \* \* e \* \* \* \* \* \* \* \* \_ notifica chiave \* \* \* \* accesso.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-122">Combination of \*\*\*\*KEY\_QUERY\_VALUE\*\*\*\*, \*\*\*\*KEY\_ENUMERATE\_SUB\_KEYS\*\*\*\*, and \*\*\*\*KEY\_NOTIFY\*\*\*\* access.</span></span><br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <span data-ttu-id="ee8d8-123"><dt>**\_valore del set di chiavi \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-123"><dt>**KEY\_SET\_VALUE**</dt></span></span> </dl>                             | <span data-ttu-id="ee8d8-124">Autorizzazione per impostare i dati della sottochiave.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-124">Permission to set subkey data.</span></span><br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <span data-ttu-id="ee8d8-125"><dt>**\_scrittura chiave**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-125"><dt>**KEY\_WRITE**</dt></span></span> </dl>                                          | <span data-ttu-id="ee8d8-126">Combinazione di \* \* \* \* valore del set di chiavi \_ \_ \* \* \* \* e \* \* \* \* chiave \_ creazione della \_ \_ sottochiave \* \* \* \* accesso.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-126">Combination of \*\*\*\*KEY\_SET\_VALUE\*\*\*\* and \*\*\*\*KEY\_CREATE\_SUB\_KEY\*\*\*\* access.</span></span><br/>                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="ee8d8-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee8d8-127">Remarks</span></span>

<span data-ttu-id="ee8d8-128">Un valore **REGSAM** può essere costituito da uno o più valori elencati.</span><span class="sxs-lookup"><span data-stu-id="ee8d8-128">A **REGSAM** value can be one or more of the listed values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8d8-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee8d8-129">Requirements</span></span>



| <span data-ttu-id="ee8d8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee8d8-130">Requirement</span></span> | <span data-ttu-id="ee8d8-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ee8d8-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8d8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee8d8-132">Header</span></span><br/> | <dl> <span data-ttu-id="ee8d8-133"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d8-133"><dt>Winnt.h</dt></span></span> </dl> |



 

 




