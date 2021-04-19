---
description: I lettori sono dispositivi standard in un sistema di smart card. Sono controllati tramite driver e vengono introdotti e rimossi dal sistema tramite Plug and Play o tramite l'elemento dispositivi del pannello di controllo.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Lettori di smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316225"
---
# <a name="smart-card-readers"></a><span data-ttu-id="89d91-104">Lettori di smart card</span><span class="sxs-lookup"><span data-stu-id="89d91-104">Smart Card Readers</span></span>

<span data-ttu-id="89d91-105">I lettori sono dispositivi standard in un sistema di [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="89d91-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="89d91-106">Sono controllati tramite driver e vengono introdotti e rimossi dal sistema tramite Plug and Play o tramite l'elemento dispositivi del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="89d91-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="89d91-107">Ogni lettore deve essere definito per l'uso da parte del [*sottosistema Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="89d91-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="89d91-108">Il sottosistema non è responsabile di alcun lettore non fornito in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="89d91-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="89d91-109">I lettori di smart card possono essere divisi in gruppi logici denominati gruppi di Reader.</span><span class="sxs-lookup"><span data-stu-id="89d91-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="89d91-110">Questi gruppi possono essere definiti dal sottosistema, nonché definiti da amministratori e utenti.</span><span class="sxs-lookup"><span data-stu-id="89d91-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="89d91-111">Un reader può appartenere a più di un gruppo di Reader</span><span class="sxs-lookup"><span data-stu-id="89d91-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="89d91-112">Il sottosistema Smart Card definisce i gruppi seguenti.</span><span class="sxs-lookup"><span data-stu-id="89d91-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="89d91-113">Gruppo</span><span class="sxs-lookup"><span data-stu-id="89d91-113">Group</span></span>                | <span data-ttu-id="89d91-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89d91-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d91-115">$ AllReaders spaventato</span><span class="sxs-lookup"><span data-stu-id="89d91-115">SCard$AllReaders</span></span>     | <span data-ttu-id="89d91-116">Questo gruppo contiene tutti i lettori del sistema.</span><span class="sxs-lookup"><span data-stu-id="89d91-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="89d91-117">Un nuovo lettore assegnato al sottosistema smart card viene incluso automaticamente nel gruppo di lettori a livello di sistema, SCard $ AllReaders.</span><span class="sxs-lookup"><span data-stu-id="89d91-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="89d91-118">$ DefaultReaders spaventato</span><span class="sxs-lookup"><span data-stu-id="89d91-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="89d91-119">Questo gruppo predefinito, uno per ogni [*terminale*](../secgloss/t-gly.md), contiene tutti i lettori assegnati al terminale che non sono riservati per un uso specifico.</span><span class="sxs-lookup"><span data-stu-id="89d91-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
