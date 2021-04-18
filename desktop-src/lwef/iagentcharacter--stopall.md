---
title: StopAll IAgentCharacter
description: StopAll IAgentCharacter
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298644"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="d6724-103">IAgentCharacter:: StopAll</span><span class="sxs-lookup"><span data-stu-id="d6724-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="d6724-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6724-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="d6724-105">Arresta tutte le animazioni (richieste) e le rimuove dalla coda di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="d6724-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="d6724-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="d6724-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="d6724-107">Oggetto bit che indica i tipi di richieste da arrestare (e rimuovere dalla coda del carattere), costituite da quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d6724-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6724-108">tipo Stop **Long senza segno const** **\_ \_ All = 0xFFFFFFFF;**</span><span class="sxs-lookup"><span data-stu-id="d6724-108">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="d6724-109">Arresta tutte le richieste di animazione, incluse le richieste di [**preparazione**](iagentcharacter--prepare.md) non in coda.</span><span class="sxs-lookup"><span data-stu-id="d6724-109">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="d6724-110">tipo di arresto **lungo senza segno const** **\_ \_ = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="d6724-110">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="d6724-111">Arresta tutte le richieste di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d6724-111">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="d6724-112">spostamento del tipo di arresto **lungo senza segno const** **\_ \_ = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="d6724-112">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="d6724-113">Arresta tutte le richieste di [**spostamento**](https://www.bing.com/search?q=**Move**) .</span><span class="sxs-lookup"><span data-stu-id="d6724-113">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="d6724-114">tipo di arresto **lungo senza segno const** **\_ \_ = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="d6724-114">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="d6724-115">Arresta tutte le richieste di [**pronuncia**](iagentcharacter--speak.md) .</span><span class="sxs-lookup"><span data-stu-id="d6724-115">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="d6724-116">tipo di arresto **lungo senza segno const** **\_ \_ Prepare = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="d6724-116">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="d6724-117">Arresta tutte le richieste di [**preparazione**](iagentcharacter--prepare.md) in coda.</span><span class="sxs-lookup"><span data-stu-id="d6724-117">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="d6724-118">tipo di arresto **lungo senza segno const** **\_ \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="d6724-118">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="d6724-119">Arresta tutte le richieste di [**preparazione**](iagentcharacter--prepare.md) non in coda.</span><span class="sxs-lookup"><span data-stu-id="d6724-119">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="d6724-120">tipo di arresto **lungo senza segno const** **\_ \_ visibile = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="d6724-120">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="d6724-121">Arresta tutte le richieste [**Nascondi**](iagentcharacter--hide.md) o [**Mostra**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="d6724-121">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d6724-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d6724-122">See Also</span></span>

[<span data-ttu-id="d6724-123">**IAgentCharacter:: Stop**</span><span class="sxs-lookup"><span data-stu-id="d6724-123">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





