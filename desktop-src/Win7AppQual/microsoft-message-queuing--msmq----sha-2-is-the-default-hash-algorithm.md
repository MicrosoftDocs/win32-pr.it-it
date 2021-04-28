---
description: "Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito"
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: "Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088099"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="324cb-103">Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito</span><span class="sxs-lookup"><span data-stu-id="324cb-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="324cb-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="324cb-104">Affected Platforms</span></span>

 <span data-ttu-id="324cb-105">**Client** - Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="324cb-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="324cb-106">**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="324cb-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="324cb-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="324cb-107">Feature Impact</span></span>

 <span data-ttu-id="324cb-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="324cb-108">**Severity** - Low</span></span>  
<span data-ttu-id="324cb-109">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="324cb-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="324cb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="324cb-110">Description</span></span>

<span data-ttu-id="324cb-111">In Windows 7, MSMQ usa SHA-2 come impostazione predefinita per la firma di un messaggio in uscita.</span><span class="sxs-lookup"><span data-stu-id="324cb-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="324cb-112">Inoltre, tutti i messaggi in ingresso devono essere firmati con SHA-2.</span><span class="sxs-lookup"><span data-stu-id="324cb-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="324cb-113">È possibile abilitare il supporto per un algoritmo di crittografia inferiore tramite una chiave del Registro di sistema accessibile dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="324cb-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="324cb-114">Manifestazione di impatto</span><span class="sxs-lookup"><span data-stu-id="324cb-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="324cb-115">MSMQ in Windows 2003 o versioni seguenti non accetterà messaggi firmati provenienti da MSMQ in Windows 7</span><span class="sxs-lookup"><span data-stu-id="324cb-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="324cb-116">MSMQ in Windows 7 non accetterà messaggi firmati provenienti da Windows 2008 o versioni seguenti</span><span class="sxs-lookup"><span data-stu-id="324cb-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="324cb-117">Mitigazione</span><span class="sxs-lookup"><span data-stu-id="324cb-117">Mitigation</span></span>

<span data-ttu-id="324cb-118">Gli utenti devono prendere in considerazione l'aggiornamento a Windows 7 per sfruttare l'algoritmo di firma più avanzato.</span><span class="sxs-lookup"><span data-stu-id="324cb-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="324cb-119">Per abilitare lo scambio di messaggi firmati senza interruzioni tra Windows 7 e qualsiasi sistema operativo di livello inferiore, l'amministratore deve aggiungere le eccezioni appropriate nei computer MSMQ.</span><span class="sxs-lookup"><span data-stu-id="324cb-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



