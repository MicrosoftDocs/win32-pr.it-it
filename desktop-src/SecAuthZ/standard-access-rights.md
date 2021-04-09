---
description: Ogni tipo di oggetto a protezione diretta dispone di un set di diritti di accesso che corrispondono alle operazioni specifiche per quel tipo di oggetto.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Diritti di accesso standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879646"
---
# <a name="standard-access-rights"></a><span data-ttu-id="d80d9-103">Diritti di accesso standard</span><span class="sxs-lookup"><span data-stu-id="d80d9-103">Standard Access Rights</span></span>

<span data-ttu-id="d80d9-104">Ogni tipo di oggetto a protezione diretta dispone di un set di diritti di accesso che corrispondono alle operazioni specifiche per quel tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d80d9-104">Each type of securable object has a set of access rights that correspond to operations specific to that type of object.</span></span> <span data-ttu-id="d80d9-105">Oltre a questi diritti di accesso specifici per gli oggetti, è disponibile un set di diritti di accesso standard che corrispondono alle operazioni comuni alla maggior parte dei tipi di oggetti a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="d80d9-105">In addition to these object-specific access rights, there is a set of standard access rights that correspond to operations common to most types of securable objects.</span></span>

<span data-ttu-id="d80d9-106">Il [formato della maschera di accesso](access-mask-format.md) include un set di bit per i diritti di accesso standard.</span><span class="sxs-lookup"><span data-stu-id="d80d9-106">The [access mask format](access-mask-format.md) includes a set of bits for the standard access rights.</span></span> <span data-ttu-id="d80d9-107">Le costanti di Windows seguenti per i diritti di accesso standard sono definite in Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="d80d9-107">The following Windows constants for standard access rights are defined in Winnt.h.</span></span>



| <span data-ttu-id="d80d9-108">Costante</span><span class="sxs-lookup"><span data-stu-id="d80d9-108">Constant</span></span>      | <span data-ttu-id="d80d9-109">Significato</span><span class="sxs-lookup"><span data-stu-id="d80d9-109">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d80d9-110">DELETE</span><span class="sxs-lookup"><span data-stu-id="d80d9-110">DELETE</span></span>        | <span data-ttu-id="d80d9-111">Diritto di eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d80d9-111">The right to delete the object.</span></span>                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d80d9-112">controllo di lettura \_</span><span class="sxs-lookup"><span data-stu-id="d80d9-112">READ\_CONTROL</span></span> | <span data-ttu-id="d80d9-113">Diritto di leggere le informazioni nel [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly)dell'oggetto, senza includere le informazioni nell' [*elenco di controllo di accesso di sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="d80d9-113">The right to read the information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), not including the information in the [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> |
| <span data-ttu-id="d80d9-114">SYNCHRONIZE</span><span class="sxs-lookup"><span data-stu-id="d80d9-114">SYNCHRONIZE</span></span>   | <span data-ttu-id="d80d9-115">Diritto di utilizzare l'oggetto per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d80d9-115">The right to use the object for synchronization.</span></span> <span data-ttu-id="d80d9-116">Ciò consente a un thread di attendere fino a quando l'oggetto non è nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="d80d9-116">This enables a thread to wait until the object is in the signaled state.</span></span> <span data-ttu-id="d80d9-117">Alcuni tipi di oggetto non supportano questo diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="d80d9-117">Some object types do not support this access right.</span></span>                                                                                                                                                                |
| <span data-ttu-id="d80d9-118">Scrivi \_ DAC</span><span class="sxs-lookup"><span data-stu-id="d80d9-118">WRITE\_DAC</span></span>    | <span data-ttu-id="d80d9-119">Diritto di modificare l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) nel descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d80d9-119">The right to modify the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) in the object's security descriptor.</span></span>                                                                                                                    |
| <span data-ttu-id="d80d9-120">Scrivi \_ proprietario</span><span class="sxs-lookup"><span data-stu-id="d80d9-120">WRITE\_OWNER</span></span>  | <span data-ttu-id="d80d9-121">Diritto di cambiare il proprietario nel descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d80d9-121">The right to change the owner in the object's security descriptor.</span></span>                                                                                                                                                                                                                                                                           |



 

<span data-ttu-id="d80d9-122">Winnt. h definisce inoltre le seguenti combinazioni di costanti dei diritti di accesso standard.</span><span class="sxs-lookup"><span data-stu-id="d80d9-122">Winnt.h also defines the following combinations of the standard access rights constants.</span></span>



| <span data-ttu-id="d80d9-123">Costante</span><span class="sxs-lookup"><span data-stu-id="d80d9-123">Constant</span></span>                   | <span data-ttu-id="d80d9-124">Significato</span><span class="sxs-lookup"><span data-stu-id="d80d9-124">Meaning</span></span>                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d80d9-125">\_tutti i diritti standard \_</span><span class="sxs-lookup"><span data-stu-id="d80d9-125">STANDARD\_RIGHTS\_ALL</span></span>      | <span data-ttu-id="d80d9-126">Combina DELETE, READ \_ Control, Write \_ DAC, Write \_ Owner e Synchronize Access.</span><span class="sxs-lookup"><span data-stu-id="d80d9-126">Combines DELETE, READ\_CONTROL, WRITE\_DAC, WRITE\_OWNER, and SYNCHRONIZE access.</span></span> |
| <span data-ttu-id="d80d9-127">\_diritti di \_ esecuzione standard</span><span class="sxs-lookup"><span data-stu-id="d80d9-127">STANDARD\_RIGHTS\_EXECUTE</span></span>  | <span data-ttu-id="d80d9-128">Attualmente definito per il controllo di lettura uguale \_ .</span><span class="sxs-lookup"><span data-stu-id="d80d9-128">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="d80d9-129">\_diritti di \_ lettura standard</span><span class="sxs-lookup"><span data-stu-id="d80d9-129">STANDARD\_RIGHTS\_READ</span></span>     | <span data-ttu-id="d80d9-130">Attualmente definito per il controllo di lettura uguale \_ .</span><span class="sxs-lookup"><span data-stu-id="d80d9-130">Currently defined to equal READ\_CONTROL.</span></span>                                         |
| <span data-ttu-id="d80d9-131">\_diritti standard \_ richiesti</span><span class="sxs-lookup"><span data-stu-id="d80d9-131">STANDARD\_RIGHTS\_REQUIRED</span></span> | <span data-ttu-id="d80d9-132">Combina l'accesso DELETE, READ \_ Control, Write \_ DAC e Write \_ owner.</span><span class="sxs-lookup"><span data-stu-id="d80d9-132">Combines DELETE, READ\_CONTROL, WRITE\_DAC, and WRITE\_OWNER access.</span></span>              |
| <span data-ttu-id="d80d9-133">\_scrittura diritti \_ standard</span><span class="sxs-lookup"><span data-stu-id="d80d9-133">STANDARD\_RIGHTS\_WRITE</span></span>    | <span data-ttu-id="d80d9-134">Attualmente definito per il controllo di lettura uguale \_ .</span><span class="sxs-lookup"><span data-stu-id="d80d9-134">Currently defined to equal READ\_CONTROL.</span></span>                                         |



 

 

 
