---
description: Utilizzato con il metodo Store. Open per indicare la modalità di apertura di un archivio certificati.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Enumerazione CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331049"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="cc54a-103">\_Enumerazione della modalità di apertura dell'archivio CAPICOM \_ \_</span><span class="sxs-lookup"><span data-stu-id="cc54a-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="cc54a-104">Il \_ \_ tipo di enumerazione di archivio CAPICOM \_ viene usato con il metodo [**Store. Open**](store-open.md) per indicare la modalità di apertura di un archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="cc54a-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="cc54a-105">Membri</span><span class="sxs-lookup"><span data-stu-id="cc54a-105">Members</span></span>



| <span data-ttu-id="cc54a-106">Membro</span><span class="sxs-lookup"><span data-stu-id="cc54a-106">Member</span></span>                                      | <span data-ttu-id="cc54a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc54a-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="cc54a-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cc54a-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="cc54a-109">**\_Archivio CAPICOM aperto in \_ \_ sola lettura \_**</span><span class="sxs-lookup"><span data-stu-id="cc54a-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="cc54a-110">Aprire l'archivio in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cc54a-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="cc54a-111">0</span><span class="sxs-lookup"><span data-stu-id="cc54a-111">0</span></span>     |
| <span data-ttu-id="cc54a-112">**\_Archivio CAPICOM \_ aperto lettura/ \_ \_ scrittura**</span><span class="sxs-lookup"><span data-stu-id="cc54a-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="cc54a-113">Aprire l'archivio in modalità di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cc54a-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="cc54a-114">1</span><span class="sxs-lookup"><span data-stu-id="cc54a-114">1</span></span>     |
| <span data-ttu-id="cc54a-115">**\_ \_ \_ massimo \_ consentito per l'archivio CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="cc54a-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="cc54a-116">Aprire l'archivio in modalità di lettura/scrittura se l'utente dispone di autorizzazioni di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cc54a-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="cc54a-117">Se l'utente non dispone di autorizzazioni di lettura/scrittura, aprire l'archivio in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cc54a-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="cc54a-118">2</span><span class="sxs-lookup"><span data-stu-id="cc54a-118">2</span></span>     |
| <span data-ttu-id="cc54a-119">**\_Archivio CAPICOM \_ aperto \_ \_ solo esistente**</span><span class="sxs-lookup"><span data-stu-id="cc54a-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="cc54a-120">Apri solo archivi esistenti; non creare un nuovo archivio.</span><span class="sxs-lookup"><span data-stu-id="cc54a-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="cc54a-121">Introdotta da capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="cc54a-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="cc54a-122">128</span><span class="sxs-lookup"><span data-stu-id="cc54a-122">128</span></span>   |
| <span data-ttu-id="cc54a-123">**\_ \_ Archivio CAPICOM aperto \_ include \_ archiviato**</span><span class="sxs-lookup"><span data-stu-id="cc54a-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="cc54a-124">Includere i certificati archiviati quando si usa l'archivio.</span><span class="sxs-lookup"><span data-stu-id="cc54a-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="cc54a-125">Introdotta da capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="cc54a-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="cc54a-126">256</span><span class="sxs-lookup"><span data-stu-id="cc54a-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="cc54a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc54a-127">Remarks</span></span>

<span data-ttu-id="cc54a-128">Quando si usa l'enumerazione dell'archivio capicot \_ \_ \_ , è possibile usare solo una delle impostazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc54a-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="cc54a-129">\_Archivio CAPICOM aperto in \_ \_ sola lettura \_</span><span class="sxs-lookup"><span data-stu-id="cc54a-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="cc54a-130">\_Archivio CAPICOM \_ aperto lettura/ \_ \_ scrittura</span><span class="sxs-lookup"><span data-stu-id="cc54a-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="cc54a-131">\_ \_ \_ massimo \_ consentito per l'archivio CAPICOM</span><span class="sxs-lookup"><span data-stu-id="cc54a-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="cc54a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc54a-132">Requirements</span></span>



| <span data-ttu-id="cc54a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc54a-133">Requirement</span></span> | <span data-ttu-id="cc54a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="cc54a-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc54a-135">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cc54a-135">Redistributable</span></span><br/> | <span data-ttu-id="cc54a-136">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="cc54a-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="cc54a-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc54a-137">Header</span></span><br/>          | <dl> <span data-ttu-id="cc54a-138"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc54a-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc54a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc54a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc54a-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="cc54a-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




