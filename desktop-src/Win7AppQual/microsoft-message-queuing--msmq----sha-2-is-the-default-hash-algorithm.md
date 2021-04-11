---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: "Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232917"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="5e9a8-103">Microsoft Message Queuing (MSMQ): SHA 2 è l'algoritmo hash predefinito</span><span class="sxs-lookup"><span data-stu-id="5e9a8-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="5e9a8-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="5e9a8-104">Affected Platforms</span></span>

 <span data-ttu-id="5e9a8-105">**Client** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="5e9a8-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="5e9a8-106">**Server** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5e9a8-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="5e9a8-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="5e9a8-107">Feature Impact</span></span>

 <span data-ttu-id="5e9a8-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="5e9a8-108">**Severity** - Low</span></span>  
<span data-ttu-id="5e9a8-109">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="5e9a8-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="5e9a8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e9a8-110">Description</span></span>

<span data-ttu-id="5e9a8-111">In Windows 7, MSMQ USA SHA-2 come impostazione predefinita per la firma di un messaggio in uscita.</span><span class="sxs-lookup"><span data-stu-id="5e9a8-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="5e9a8-112">Inoltre, tutti i messaggi in arrivo devono essere firmati con SHA-2.</span><span class="sxs-lookup"><span data-stu-id="5e9a8-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="5e9a8-113">È possibile abilitare il supporto per un algoritmo di crittografia inferiore tramite una chiave del registro di sistema accessibile dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="5e9a8-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="5e9a8-114">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="5e9a8-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="5e9a8-115">MSMQ in Windows 2003 o versioni precedenti non accetterà i messaggi firmati provenienti da MSMQ in Windows 7</span><span class="sxs-lookup"><span data-stu-id="5e9a8-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="5e9a8-116">MSMQ in Windows 7 non accetterà i messaggi firmati provenienti da Windows 2008 o versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="5e9a8-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="5e9a8-117">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="5e9a8-117">Mitigation</span></span>

<span data-ttu-id="5e9a8-118">Gli utenti devono prendere in considerazione l'aggiornamento a Windows 7 per sfruttare l'algoritmo di firma più solido.</span><span class="sxs-lookup"><span data-stu-id="5e9a8-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="5e9a8-119">Per consentire lo scambio di messaggi firmato senza problemi tra Windows 7 e qualsiasi sistema operativo di livello inferiore, l'amministratore deve aggiungere le eccezioni appropriate nei computer MSMQ.</span><span class="sxs-lookup"><span data-stu-id="5e9a8-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



