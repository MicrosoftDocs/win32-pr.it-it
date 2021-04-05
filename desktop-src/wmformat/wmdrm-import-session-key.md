---
title: Struttura WMDRM_IMPORT_SESSION_KEY (Drmexternals. h)
description: La \_ struttura della \_ chiave della sessione di importazione WMDRM \_ include la chiave della sessione per l'importazione del contenuto protetto.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Formato di Windows Media per la struttura WMDRM_IMPORT_SESSION_KEY
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120854"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="23e28-105">WMDRM \_ importare \_ la \_ struttura della chiave della sessione</span><span class="sxs-lookup"><span data-stu-id="23e28-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="23e28-106">La struttura della **\_ chiave della \_ sessione \_ di importazione WMDRM** include la chiave della sessione per l'importazione del contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="23e28-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e28-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23e28-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="23e28-108">Members</span><span class="sxs-lookup"><span data-stu-id="23e28-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="23e28-109">**dwKeyType**</span><span class="sxs-lookup"><span data-stu-id="23e28-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="23e28-110">Tipo di chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="23e28-110">Session key type.</span></span> <span data-ttu-id="23e28-111">Impostare su WMDRM di \_ tipo \_ RC4.</span><span class="sxs-lookup"><span data-stu-id="23e28-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="23e28-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="23e28-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="23e28-113">Dimensione, in byte, della chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="23e28-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="23e28-114">Questo valore può essere il più grande necessario, dati i limiti di una singola operazione RSA OAEP sull'intero messaggio (la struttura più la chiave della sessione).</span><span class="sxs-lookup"><span data-stu-id="23e28-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="23e28-115">**rgbKey**</span><span class="sxs-lookup"><span data-stu-id="23e28-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="23e28-116">Indirizzo di un buffer contenente la chiave della sessione.</span><span class="sxs-lookup"><span data-stu-id="23e28-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="23e28-117">Le dimensioni del buffer devono corrispondere al valore di **cbKey**.</span><span class="sxs-lookup"><span data-stu-id="23e28-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="23e28-118">I dati nel buffer sono un valore di chiave generato in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="23e28-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23e28-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="23e28-119">Remarks</span></span>

<span data-ttu-id="23e28-120">Questa struttura, incluso il buffer contenente la chiave della sessione, deve essere crittografata con la chiave pubblica del computer DRM di Windows Media e inclusa nel membro **pbEncryptedSessionKeyMessage** della struttura dello [**\_ \_ \_ struct di importazione WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="23e28-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e28-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23e28-121">Requirements</span></span>



| <span data-ttu-id="23e28-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e28-122">Requirement</span></span> | <span data-ttu-id="23e28-123">Valore</span><span class="sxs-lookup"><span data-stu-id="23e28-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e28-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23e28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="23e28-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="23e28-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="23e28-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23e28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="23e28-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23e28-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="23e28-128">Versione</span><span class="sxs-lookup"><span data-stu-id="23e28-128">Version</span></span><br/>                  | <span data-ttu-id="23e28-129">SDK di Windows Media Format 11</span><span class="sxs-lookup"><span data-stu-id="23e28-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="23e28-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23e28-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="23e28-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e28-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e28-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23e28-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e28-133">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="23e28-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





