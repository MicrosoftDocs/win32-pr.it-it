---
title: Oggetto Principal
description: Oggetto di scripting che fornisce le credenziali di sicurezza per un'entità.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Utilità di pianificazione oggetto principale
- Utilità di pianificazione oggetto principale, descritto
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873553"
---
# <a name="principal-object"></a><span data-ttu-id="3befb-105">Oggetto Principal</span><span class="sxs-lookup"><span data-stu-id="3befb-105">Principal object</span></span>

<span data-ttu-id="3befb-106">Oggetto di scripting che fornisce le credenziali di sicurezza per un'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="3befb-107">Queste credenziali di sicurezza definiscono il contesto di sicurezza per le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="3befb-108">Membri</span><span class="sxs-lookup"><span data-stu-id="3befb-108">Members</span></span>

<span data-ttu-id="3befb-109">L'oggetto **Principal** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3befb-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="3befb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3befb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3befb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3befb-111">Properties</span></span>

<span data-ttu-id="3befb-112">L'oggetto **Principal** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3befb-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="3befb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3befb-113">Property</span></span>                                                | <span data-ttu-id="3befb-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="3befb-114">Access type</span></span>           | <span data-ttu-id="3befb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3befb-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3befb-116">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="3befb-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="3befb-117">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3befb-117">Read/write</span></span><br/> | <span data-ttu-id="3befb-118">Ottiene o imposta il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3befb-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="3befb-119">**GroupId**</span><span class="sxs-lookup"><span data-stu-id="3befb-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="3befb-120">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3befb-120">Read/write</span></span><br/> | <span data-ttu-id="3befb-121">Ottiene o imposta l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="3befb-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="3befb-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="3befb-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3befb-123">Read/write</span></span><br/> | <span data-ttu-id="3befb-124">Ottiene o imposta l'identificatore dell'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="3befb-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="3befb-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="3befb-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3befb-126">Read/write</span></span><br/> | <span data-ttu-id="3befb-127">Ottiene o imposta il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="3befb-128">**RunLevel**</span><span class="sxs-lookup"><span data-stu-id="3befb-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="3befb-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3befb-129">Read/write</span></span><br/> | <span data-ttu-id="3befb-130">Ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="3befb-131">**UserId**</span><span class="sxs-lookup"><span data-stu-id="3befb-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="3befb-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="3befb-132">Read/write</span></span><br/> | <span data-ttu-id="3befb-133">Ottiene o imposta l'identificatore utente necessario per eseguire le attività associate all'entità.</span><span class="sxs-lookup"><span data-stu-id="3befb-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="3befb-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="3befb-134">Remarks</span></span>

<span data-ttu-id="3befb-135">Quando si specifica un account, ricordarsi di usare correttamente la doppia barra rovesciata nel codice per specificare il dominio e il nome utente.</span><span class="sxs-lookup"><span data-stu-id="3befb-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="3befb-136">Usare, ad esempio, DOMAIN \\ \\ username per specificare un valore per la proprietà [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="3befb-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="3befb-137">Durante la lettura o la scrittura di codice XML per un'attività, le credenziali di sicurezza per un'entità vengono specificate nell'elemento [**Principal**](taskschedulerschema-principal-principaltype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="3befb-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="3befb-138">Se un'attività viene registrata usando lo strumento da riga di comando at.exe e questo oggetto viene usato per recuperare informazioni sull'attività, la proprietà [**LogonType**](principal-logontype.md) restituirà 0, la proprietà [**runlevel**](principal-runlevel.md) restituirà 0 e la proprietà [**userid**](principal-userid.md) non restituirà alcun valore.</span><span class="sxs-lookup"><span data-stu-id="3befb-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="3befb-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="3befb-139">Examples</span></span>

<span data-ttu-id="3befb-140">Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="3befb-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3befb-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3befb-141">Requirements</span></span>



| <span data-ttu-id="3befb-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3befb-142">Requirement</span></span> | <span data-ttu-id="3befb-143">Valore</span><span class="sxs-lookup"><span data-stu-id="3befb-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3befb-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3befb-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3befb-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3befb-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3befb-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3befb-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3befb-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3befb-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3befb-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3befb-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="3befb-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3befb-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3befb-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3befb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3befb-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3befb-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





