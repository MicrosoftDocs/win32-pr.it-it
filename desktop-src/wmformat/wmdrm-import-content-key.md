---
title: Struttura WMDRM_IMPORT_CONTENT_KEY (Drmexternals. h)
description: La \_ struttura della chiave simmetrica di importazione WMDRM \_ \_ Archivia la chiave simmetrica usata per l'importazione del contenuto protetto.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Formato di Windows Media per la struttura WMDRM_IMPORT_CONTENT_KEY
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400290"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="164aa-105">WMDRM \_ importare \_ la \_ struttura della chiave simmetrica</span><span class="sxs-lookup"><span data-stu-id="164aa-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="164aa-106">La struttura della **\_ \_ \_ chiave simmetrica di importazione WMDRM** archivia la chiave simmetrica usata per l'importazione del contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="164aa-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="164aa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="164aa-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="164aa-108">Members</span><span class="sxs-lookup"><span data-stu-id="164aa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="164aa-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="164aa-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-110">Versione.</span><span class="sxs-lookup"><span data-stu-id="164aa-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="164aa-111">**cbStructSize**</span><span class="sxs-lookup"><span data-stu-id="164aa-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-112">Dimensione della struttura in byte.</span><span class="sxs-lookup"><span data-stu-id="164aa-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="164aa-113">**dwIVKeyType**</span><span class="sxs-lookup"><span data-stu-id="164aa-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-114">Tipo di chiave del vettore di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="164aa-114">Initialization vector key type.</span></span> <span data-ttu-id="164aa-115">Impostare su WMDRM di \_ tipo \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="164aa-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="164aa-116">**cbIVKey**</span><span class="sxs-lookup"><span data-stu-id="164aa-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-117">Dimensioni in byte della chiave del vettore di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="164aa-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="164aa-118">**dwContentKeyType**</span><span class="sxs-lookup"><span data-stu-id="164aa-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-119">Tipo di chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="164aa-119">Content key type.</span></span> <span data-ttu-id="164aa-120">Impostare su WMDRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="164aa-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="164aa-121">**cbContentKey**</span><span class="sxs-lookup"><span data-stu-id="164aa-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-122">Dimensioni in byte della chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="164aa-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="164aa-123">**rgbKeyData**</span><span class="sxs-lookup"><span data-stu-id="164aa-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="164aa-124">Indirizzo di un buffer contenente la chiave simmetrica.</span><span class="sxs-lookup"><span data-stu-id="164aa-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="164aa-125">Le dimensioni del buffer devono corrispondere al valore di **cbContentKey**.</span><span class="sxs-lookup"><span data-stu-id="164aa-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="164aa-126">Questa chiave deve corrispondere alla chiave importata dal messaggio di licenza XMR.</span><span class="sxs-lookup"><span data-stu-id="164aa-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="164aa-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="164aa-127">Remarks</span></span>

<span data-ttu-id="164aa-128">Questa struttura, incluso il buffer contenente la chiave della sessione, deve essere crittografata con la chiave della sessione e inclusa nel membro **pbEncryptedKeyMessage** della struttura dello [**\_ \_ \_ struct di importazione WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="164aa-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="164aa-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="164aa-129">Requirements</span></span>



| <span data-ttu-id="164aa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="164aa-130">Requirement</span></span> | <span data-ttu-id="164aa-131">Valore</span><span class="sxs-lookup"><span data-stu-id="164aa-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="164aa-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="164aa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="164aa-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="164aa-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="164aa-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="164aa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="164aa-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="164aa-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="164aa-136">Versione</span><span class="sxs-lookup"><span data-stu-id="164aa-136">Version</span></span><br/>                  | <span data-ttu-id="164aa-137">SDK di Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="164aa-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="164aa-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="164aa-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="164aa-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="164aa-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164aa-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="164aa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164aa-141">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="164aa-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





