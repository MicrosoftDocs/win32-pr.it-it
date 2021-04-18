---
description: I valori definiscono un tipo di firma di accesso condiviso specifico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315846"
---
# <a name="wlx_sas_type_xxx"></a><span data-ttu-id="62f13-103">WLX \_ SAS \_ tipo \_ xxx</span><span class="sxs-lookup"><span data-stu-id="62f13-103">WLX\_SAS\_TYPE\_XXX</span></span>

<span data-ttu-id="62f13-104">\[La \_ \_ \_ costante di tipo xxx della firma di accesso condiviso non è più disponibile per l'uso a partire da Windows Server 2008 e Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="62f13-104">\[The WLX\_SAS\_TYPE\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="62f13-105">I valori di **\_ \_ tipo \_ xxx** di firma di accesso condiviso definiscono un tipo di firma di accesso condiviso specifico</span><span class="sxs-lookup"><span data-stu-id="62f13-105">The **WLX\_SAS\_TYPE\_XXX** values define a specific SAS type.</span></span>

> [!Note]  
> <span data-ttu-id="62f13-106">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62f13-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="62f13-107">Tutti i valori da zero a 127 sono riservati ai tipi definiti da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62f13-107">All values from zero to 127 are reserved for Microsoft-defined types.</span></span> <span data-ttu-id="62f13-108">I valori superiori a 127 sono disponibili per i tipi definiti dal cliente.</span><span class="sxs-lookup"><span data-stu-id="62f13-108">Values above 127 are available for customer-defined types.</span></span> <span data-ttu-id="62f13-109">I tipi seguenti vengono passati alle funzioni che hanno un parametro *dwSasType* .</span><span class="sxs-lookup"><span data-stu-id="62f13-109">The following types are passed to functions that have a *dwSasType* parameter.</span></span>



| <span data-ttu-id="62f13-110">Costante</span><span class="sxs-lookup"><span data-stu-id="62f13-110">Constant</span></span>                                                                                                                                                                                                         | <span data-ttu-id="62f13-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62f13-111">Description</span></span>                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <span data-ttu-id="62f13-112"><dt>**tipo di firma di accesso condiviso di WLX \_ \_ \_ CTRL \_ ALT \_ Canc**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-112"><dt>**WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL**</dt></span></span> </dl>            | <span data-ttu-id="62f13-113">Indica che un utente ha digitato la firma di accesso condiviso standard CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="62f13-113">Indicates a user has typed the standard CTRL+ALT+DEL SAS.</span></span><br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <span data-ttu-id="62f13-114"><dt>**tipo di firma di accesso condiviso di WLX \_ SAS \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-114"><dt>**WLX\_SAS\_TYPE\_SC\_INSERT**</dt></span></span> </dl>                      | <span data-ttu-id="62f13-115">Indica che una [*Smart Card*](../secgloss/s-gly.md) è stata inserita in un dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="62f13-115">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span><br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <span data-ttu-id="62f13-116"><dt>**tipo di firma di accesso condiviso di WLX \_ \_ \_ SC \_ Remove**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-116"><dt>**WLX\_SAS\_TYPE\_SC\_REMOVE**</dt></span></span> </dl>                      | <span data-ttu-id="62f13-117">Indica che una smart card è stata rimossa da un dispositivo compatibile.</span><span class="sxs-lookup"><span data-stu-id="62f13-117">Indicates that a smart card has been removed from a compatible device.</span></span><br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <span data-ttu-id="62f13-118"><dt>**\_ \_ attività SCRNSVR di tipo SAS \_ di \_ wlx**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-118"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_ACTIVITY**</dt></span></span> </dl> | <span data-ttu-id="62f13-119">Indica che si è verificata un'attività della tastiera o del mouse mentre era attiva una screen saver sicura.</span><span class="sxs-lookup"><span data-stu-id="62f13-119">Indicates that keyboard or mouse activity occurred while a secure screen saver was active.</span></span><br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <span data-ttu-id="62f13-120"><dt>**\_ \_ \_ timeout SCRNSVR tipo SAS \_ di wlx**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-120"><dt>**WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT**</dt></span></span> </dl>    | <span data-ttu-id="62f13-121">Indica che screen saver si è verificata l'attivazione a causa di inattività della tastiera e del mouse.</span><span class="sxs-lookup"><span data-stu-id="62f13-121">Indicates that screen saver activation has occurred due to keyboard and mouse inactivity.</span></span><br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <span data-ttu-id="62f13-122"><dt>**\_ \_ timeout tipo di SAS di WLX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-122"><dt>**WLX\_SAS\_TYPE\_TIMEOUT**</dt></span></span> </dl>                             | <span data-ttu-id="62f13-123">Indica che non è stato ricevuto alcun input da parte dell'utente entro il periodo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="62f13-123">Indicates that no user input was received within the specified time-out period.</span></span><br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <span data-ttu-id="62f13-124"><dt>**\_disconnessione \_ utente tipo di SAS \_ wlx \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-124"><dt>**WLX\_SAS\_TYPE\_USER\_LOGOFF**</dt></span></span> </dl>                | <span data-ttu-id="62f13-125">Indica che l'utente è stato disconnesso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="62f13-125">Indicates the user is being logged off the system.</span></span><br/>                                                                                            |



## <a name="requirements"></a><span data-ttu-id="62f13-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62f13-126">Requirements</span></span>



| <span data-ttu-id="62f13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f13-127">Requirement</span></span> | <span data-ttu-id="62f13-128">Valore</span><span class="sxs-lookup"><span data-stu-id="62f13-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="62f13-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f13-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62f13-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="62f13-130">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="62f13-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f13-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62f13-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62f13-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="62f13-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="62f13-133">End of client support</span></span><br/>    | <span data-ttu-id="62f13-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="62f13-134">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="62f13-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="62f13-135">End of server support</span></span><br/>    | <span data-ttu-id="62f13-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62f13-136">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="62f13-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62f13-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f13-138"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f13-138"><dt>Winwlx.h</dt></span></span> </dl> |



 

 
