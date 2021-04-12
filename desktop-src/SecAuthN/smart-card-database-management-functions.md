---
description: Gestire il database delle smart card, aggiornando il database usando un contesto di Resource Manager specificato.
ms.assetid: a2f457e1-c042-42e7-9071-cf0edd68e27a
title: Funzioni di gestione di database per Smart Card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c424494a30c71e15647da773027311ed53a2599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347306"
---
# <a name="smart-card-database-management-functions"></a><span data-ttu-id="d98c6-103">Funzioni di gestione di database per Smart Card</span><span class="sxs-lookup"><span data-stu-id="d98c6-103">Smart Card Database Management Functions</span></span>

<span data-ttu-id="d98c6-104">Le funzioni seguenti gestiscono il [*database delle smart card*](../secgloss/s-gly.md), aggiornando il database usando un [*contesto di Resource Manager*](../secgloss/r-gly.md)specificato.</span><span class="sxs-lookup"><span data-stu-id="d98c6-104">The following functions manage the [*smart card database*](../secgloss/s-gly.md), updating the database by using a specified [*resource manager context*](../secgloss/r-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="d98c6-105">La sicurezza del database viene gestita inserendo restrizioni di accesso nel database, invece di aggiungere meccanismi di sicurezza al [*sottosistema Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d98c6-105">Database security is maintained by placing access restrictions on the database, rather than by adding security mechanisms to the [*smart card subsystem*](../secgloss/s-gly.md).</span></span>

 



| <span data-ttu-id="d98c6-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="d98c6-106">Topic</span></span>                                                            | <span data-ttu-id="d98c6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d98c6-107">Description</span></span>                                                                                                                                                             |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d98c6-108">**SCardAddReaderToGroup**</span><span class="sxs-lookup"><span data-stu-id="d98c6-108">**SCardAddReaderToGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardaddreadertogroupa)           | <span data-ttu-id="d98c6-109">Aggiungere un [*Reader*](../secgloss/r-gly.md) a un [*gruppo Reader*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d98c6-109">Add a [*reader*](../secgloss/r-gly.md) to a [*reader group*](../secgloss/r-gly.md).</span></span> |
| [<span data-ttu-id="d98c6-110">**SCardForgetCardType**</span><span class="sxs-lookup"><span data-stu-id="d98c6-110">**SCardForgetCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea)               | <span data-ttu-id="d98c6-111">Rimuovere una smart card dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d98c6-111">Remove a smart card from the system.</span></span>                                                                                                                                    |
| [<span data-ttu-id="d98c6-112">**SCardForgetReader**</span><span class="sxs-lookup"><span data-stu-id="d98c6-112">**SCardForgetReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadera)                   | <span data-ttu-id="d98c6-113">Rimuovere un Reader dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d98c6-113">Remove a reader from the system.</span></span>                                                                                                                                        |
| [<span data-ttu-id="d98c6-114">**SCardForgetReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="d98c6-114">**SCardForgetReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardforgetreadergroupa)         | <span data-ttu-id="d98c6-115">Rimuovere un gruppo di Reader dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d98c6-115">Remove a reader group from the system.</span></span>                                                                                                                                  |
| [<span data-ttu-id="d98c6-116">**SCardIntroduceCardType**</span><span class="sxs-lookup"><span data-stu-id="d98c6-116">**SCardIntroduceCardType**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea)         | <span data-ttu-id="d98c6-117">Introduce una nuova scheda al sistema.</span><span class="sxs-lookup"><span data-stu-id="d98c6-117">Introduce a new card to the system.</span></span>                                                                                                                                     |
| [<span data-ttu-id="d98c6-118">**SCardIntroduceReader**</span><span class="sxs-lookup"><span data-stu-id="d98c6-118">**SCardIntroduceReader**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadera)             | <span data-ttu-id="d98c6-119">Introduce un nuovo lettore al sistema.</span><span class="sxs-lookup"><span data-stu-id="d98c6-119">Introduce a new reader to the system.</span></span>                                                                                                                                   |
| [<span data-ttu-id="d98c6-120">**SCardIntroduceReaderGroup**</span><span class="sxs-lookup"><span data-stu-id="d98c6-120">**SCardIntroduceReaderGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardintroducereadergroupa)   | <span data-ttu-id="d98c6-121">Introduce un nuovo gruppo di lettori al sistema.</span><span class="sxs-lookup"><span data-stu-id="d98c6-121">Introduce a new reader group to the system.</span></span>                                                                                                                             |
| [<span data-ttu-id="d98c6-122">**SCardRemoveReaderFromGroup**</span><span class="sxs-lookup"><span data-stu-id="d98c6-122">**SCardRemoveReaderFromGroup**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardremovereaderfromgroupa) | <span data-ttu-id="d98c6-123">Rimuovere un Reader da un gruppo di Reader.</span><span class="sxs-lookup"><span data-stu-id="d98c6-123">Remove a reader from a reader group.</span></span>                                                                                                                                    |



 

 

 
