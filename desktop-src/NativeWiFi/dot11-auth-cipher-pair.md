---
description: Definisce una coppia di algoritmi di crittografia e autenticazione 802,11 che possono essere abilitati nello stesso momento nella stazione 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Struttura DOT11_AUTH_CIPHER_PAIR (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313767"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="5c841-103">\_Struttura delle \_ coppie di crittografia auth DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="5c841-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="5c841-104">La struttura delle **\_ \_ \_ coppie di crittografia auth DOT11** definisce una coppia di algoritmi di crittografia e autenticazione 802,11 che possono essere abilitati allo stesso tempo nella stazione 802,11.</span><span class="sxs-lookup"><span data-stu-id="5c841-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c841-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c841-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="5c841-106">Members</span><span class="sxs-lookup"><span data-stu-id="5c841-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c841-107">**AuthAlgoId**</span><span class="sxs-lookup"><span data-stu-id="5c841-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="5c841-108">Algoritmo di autenticazione che usa un tipo enumerato dell' [**\_ \_ algoritmo**](dot11-auth-algorithm.md) di autenticazione DOT11.</span><span class="sxs-lookup"><span data-stu-id="5c841-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="5c841-109">**CipherAlgoId**</span><span class="sxs-lookup"><span data-stu-id="5c841-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="5c841-110">Algoritmo di crittografia che utilizza un tipo enumerato dell' [**\_ \_ algoritmo di crittografia DOT11**](dot11-cipher-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="5c841-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c841-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c841-111">Remarks</span></span>

<span data-ttu-id="5c841-112">La \_ struttura delle \_ coppie di crittografia auth DOT11 \_ definisce un algoritmo di autenticazione e crittografia che può essere abilitato insieme per le connessioni di rete di base del set di servizi (BSS).</span><span class="sxs-lookup"><span data-stu-id="5c841-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c841-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c841-113">Requirements</span></span>



| <span data-ttu-id="5c841-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c841-114">Requirement</span></span> | <span data-ttu-id="5c841-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5c841-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c841-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c841-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c841-117">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="5c841-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c841-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c841-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c841-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c841-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5c841-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5c841-120">Redistributable</span></span><br/>          | <span data-ttu-id="5c841-121">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="5c841-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="5c841-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c841-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c841-123"><dt>Wlantypes. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c841-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c841-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c841-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c841-125">**\_Algoritmo di autenticazione DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="5c841-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="5c841-126">**\_Algoritmo di crittografia DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="5c841-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




