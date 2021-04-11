---
title: PreferredServerBitness
description: Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valore PreferredServerBitness del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339358"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="17a9f-104">PreferredServerBitness</span><span class="sxs-lookup"><span data-stu-id="17a9f-104">PreferredServerBitness</span></span>

<span data-ttu-id="17a9f-105">Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.</span><span class="sxs-lookup"><span data-stu-id="17a9f-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="17a9f-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="17a9f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="17a9f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="17a9f-107">Remarks</span></span>

<span data-ttu-id="17a9f-108">Si tratta di un valore **reg \_ DWORD** disponibile solo nelle versioni di Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="17a9f-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="17a9f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="17a9f-109">Value</span></span> | <span data-ttu-id="17a9f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17a9f-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a9f-111">1</span><span class="sxs-lookup"><span data-stu-id="17a9f-111">1</span></span>     | <span data-ttu-id="17a9f-112">Abbinare l'architettura del server all'architettura client.</span><span class="sxs-lookup"><span data-stu-id="17a9f-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="17a9f-113">Se, ad esempio, il client è a 32 bit, utilizzare una versione a 32 bit del server, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="17a9f-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="17a9f-114">In caso contrario, la richiesta di attivazione del client avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="17a9f-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="17a9f-115">2</span><span class="sxs-lookup"><span data-stu-id="17a9f-115">2</span></span>     | <span data-ttu-id="17a9f-116">Usare una versione a 32 bit del server.</span><span class="sxs-lookup"><span data-stu-id="17a9f-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="17a9f-117">Se non ne esiste una, la richiesta di attivazione del client avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="17a9f-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="17a9f-118">3</span><span class="sxs-lookup"><span data-stu-id="17a9f-118">3</span></span>     | <span data-ttu-id="17a9f-119">Usare una versione a 64 bit del server.</span><span class="sxs-lookup"><span data-stu-id="17a9f-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="17a9f-120">Se non ne esiste una, la richiesta di attivazione del client avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="17a9f-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="17a9f-121">Se questo valore non è presente, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="17a9f-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="17a9f-122">Se nel computer che ospita il server è in esecuzione Windows XP o Windows Server 2003 senza SP1 o versione successiva, è preferibile a una versione a 64 bit del server, se disponibile. in caso contrario, attiverà una versione a 32 bit del server.</span><span class="sxs-lookup"><span data-stu-id="17a9f-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="17a9f-123">Se nel computer che ospita il server è in esecuzione Windows Server 2003 con SP1 o versione successiva, COM tenterà di abbinare l'architettura del server all'architettura client.</span><span class="sxs-lookup"><span data-stu-id="17a9f-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="17a9f-124">In altre parole, per un client a 32 bit, COM attiverà un server a 32 bit, se disponibile. in caso contrario, attiverà una versione a 64 bit del server.</span><span class="sxs-lookup"><span data-stu-id="17a9f-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="17a9f-125">Per un client a 64 bit, COM attiverà un server a 64 bit se disponibile; in caso contrario, attiverà un server a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="17a9f-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="17a9f-126">Il client può anche specificare la propria preferenza di architettura tramite il \_ Server CLSCTX activate \_ 32 \_ bit \_ e CLSCTX \_ Activate \_ 64 \_ bit \_ Server Flags, che sostituiranno le preferenze del server.</span><span class="sxs-lookup"><span data-stu-id="17a9f-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="17a9f-127">Per ulteriori informazioni e un grafico delle possibili interazioni tra le preferenze per l'architettura client e server, vedere [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span><span class="sxs-lookup"><span data-stu-id="17a9f-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17a9f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17a9f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17a9f-129">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="17a9f-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 