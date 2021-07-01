---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120914"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="33b99-103">IAgentCharacter::StopAll</span><span class="sxs-lookup"><span data-stu-id="33b99-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="33b99-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="33b99-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="33b99-105">Arresta tutte le animazioni (richieste) e le rimuove dalla coda di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="33b99-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="33b99-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="33b99-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="33b99-107">Campo di bit che indica i tipi di richieste da arrestare (e rimuovere dalla coda del carattere), costituite dalle seguenti:</span><span class="sxs-lookup"><span data-stu-id="33b99-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



| <span data-ttu-id="33b99-108">Valore</span><span class="sxs-lookup"><span data-stu-id="33b99-108">Value</span></span>                                                                                  |  <span data-ttu-id="33b99-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33b99-109">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b99-110">**const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="33b99-110">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="33b99-111">Arresta tutte le richieste di animazione, incluse le richieste [**di preparazione**](iagentcharacter--prepare.md) non in coda.</span><span class="sxs-lookup"><span data-stu-id="33b99-111">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="33b99-112">**const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="33b99-112">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="33b99-113">Arresta tutte le richieste di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="33b99-113">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="33b99-114">**const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="33b99-114">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="33b99-115">Arresta tutte [**le richieste Move.**](https://www.bing.com/search?q=**Move**)</span><span class="sxs-lookup"><span data-stu-id="33b99-115">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="33b99-116">**const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="33b99-116">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="33b99-117">Arresta tutte [**le richieste Speak.**](iagentcharacter--speak.md)</span><span class="sxs-lookup"><span data-stu-id="33b99-117">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="33b99-118">**const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="33b99-118">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="33b99-119">Arresta tutte le richieste [**Prepare in**](iagentcharacter--prepare.md) coda.</span><span class="sxs-lookup"><span data-stu-id="33b99-119">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="33b99-120">**const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="33b99-120">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="33b99-121">Arresta tutte le richieste [**di preparazione**](iagentcharacter--prepare.md) non in coda.</span><span class="sxs-lookup"><span data-stu-id="33b99-121">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="33b99-122">**const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="33b99-122">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="33b99-123">Arresta [**tutte le richieste Nascondi**](iagentcharacter--hide.md) [**o**](iagentcharacter--show.md) Mostra.</span><span class="sxs-lookup"><span data-stu-id="33b99-123">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="33b99-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="33b99-124">See Also</span></span>

[<span data-ttu-id="33b99-125">**IAgentCharacter::Stop**</span><span class="sxs-lookup"><span data-stu-id="33b99-125">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





