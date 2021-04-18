---
title: StorAHCI sostituisce MSAHCI
description: StorAHCI sostituisce MSAHCI
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300572"
---
# <a name="storahci-replaces-msahci"></a><span data-ttu-id="07f76-103">StorAHCI sostituisce MSAHCI</span><span class="sxs-lookup"><span data-stu-id="07f76-103">StorAHCI replaces MSAHCI</span></span>

## <a name="platforms"></a><span data-ttu-id="07f76-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="07f76-104">Platforms</span></span>

<span data-ttu-id="07f76-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="07f76-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="07f76-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07f76-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="07f76-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07f76-107">Description</span></span>

<span data-ttu-id="07f76-108">StorAHCI, un Storport miniport, supporta i controller AHCI (Advanced Host Controller Interface) SATA (Serial Advanced Technology Attachment) in Windows e sostituisce MSAHCI, un miniport ATAport.</span><span class="sxs-lookup"><span data-stu-id="07f76-108">StorAHCI, a Storport miniport, supports serial advanced technology attachment (SATA) advanced host controller interface (AHCI) controllers in Windows, and replaces MSAHCI, an ATAport miniport.</span></span>

## <a name="manifestation"></a><span data-ttu-id="07f76-109">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="07f76-109">Manifestation</span></span>

<span data-ttu-id="07f76-110">Non devono essere apportate modifiche alle funzionalità e alle prestazioni. Questo driver supporta tutti gli stessi dispositivi supportati da MSAHCI.</span><span class="sxs-lookup"><span data-stu-id="07f76-110">There should be no change in functionality or performance; this driver supports all the same devices that MSAHCI supports.</span></span>

<span data-ttu-id="07f76-111">Questa modifica è trasparente per l'utente.</span><span class="sxs-lookup"><span data-stu-id="07f76-111">This change is transparent to the user.</span></span>

## <a name="mitigation"></a><span data-ttu-id="07f76-112">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="07f76-112">Mitigation</span></span>

<span data-ttu-id="07f76-113">Aggiornare tutte le utilità e gli script basati sui binding ATAport.</span><span class="sxs-lookup"><span data-stu-id="07f76-113">Update any utilities and scripts that rely on ATAport bindings.</span></span> <span data-ttu-id="07f76-114">Non fare affidamento sul nome dell'unità.</span><span class="sxs-lookup"><span data-stu-id="07f76-114">Do not rely on the drive name.</span></span> <span data-ttu-id="07f76-115">Usare invece il rilevamento del disco standard.</span><span class="sxs-lookup"><span data-stu-id="07f76-115">Instead use standard disk detection.</span></span>

 

 




