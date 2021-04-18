---
title: Struttura WMDRMCryptoData (wmdrmsdk. h)
description: La struttura WMDRMCryptoData contiene informazioni sull'algoritmo di crittografia utilizzato per crittografare e decrittografare il contenuto.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Formato Windows Media della struttura WMDRMCryptoData
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330880"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="37957-105">Struttura WMDRMCryptoData</span><span class="sxs-lookup"><span data-stu-id="37957-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="37957-106">La struttura **WMDRMCryptoData** contiene informazioni sull'algoritmo di crittografia utilizzato per crittografare e decrittografare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="37957-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="37957-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37957-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="37957-108">Members</span><span class="sxs-lookup"><span data-stu-id="37957-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37957-109">**cryptoType**</span><span class="sxs-lookup"><span data-stu-id="37957-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="37957-110">Membro dell'enumerazione [**del \_ \_ tipo di crittografia DRM**](drm-crypto-type.md) che specifica il tipo di algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="37957-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="37957-111">**qwCounterID**</span><span class="sxs-lookup"><span data-stu-id="37957-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="37957-112">Bit 64 alti della modalità del contatore AES a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="37957-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="37957-113">Questo membro viene usato solo se il membro **cryptoType** è impostato su **Crypto \_ Type \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="37957-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="37957-114">**qwOffset**</span><span class="sxs-lookup"><span data-stu-id="37957-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="37957-115">Bit 64 bassi della modalità del contatore AES a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="37957-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="37957-116">Questo membro viene usato solo se il membro **cryptoType** è impostato su **Crypto \_ Type \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="37957-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37957-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37957-117">Requirements</span></span>



| <span data-ttu-id="37957-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="37957-118">Requirement</span></span> | <span data-ttu-id="37957-119">Valore</span><span class="sxs-lookup"><span data-stu-id="37957-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37957-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37957-120">Header</span></span><br/> | <dl> <span data-ttu-id="37957-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="37957-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37957-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37957-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37957-123">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="37957-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





