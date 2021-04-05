---
title: Proprietà RegistrationInfo. Source
description: Per gli script, ottiene o imposta la posizione da cui ha origine l'attività. Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Utilità di pianificazione proprietà di origine
- Utilità di pianificazione proprietà di origine, oggetto RegistrationInfo
- Utilità di pianificazione oggetto RegistrationInfo, proprietà Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d360a20d1f0f4736db4dd6f136a579178a65ca70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742442"
---
# <a name="registrationinfosource-property"></a><span data-ttu-id="f38b4-107">Proprietà RegistrationInfo. Source</span><span class="sxs-lookup"><span data-stu-id="f38b4-107">RegistrationInfo.Source property</span></span>

<span data-ttu-id="f38b4-108">Per gli script, ottiene o imposta la posizione da cui ha origine l'attività.</span><span class="sxs-lookup"><span data-stu-id="f38b4-108">For scripting, gets or sets where the task originated from.</span></span> <span data-ttu-id="f38b4-109">Ad esempio, un'attività può provenire da un componente, un servizio, un'applicazione o un utente.</span><span class="sxs-lookup"><span data-stu-id="f38b4-109">For example, a task may originate from a component, service, application, or user.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38b4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f38b4-110">Syntax</span></span>


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a><span data-ttu-id="f38b4-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f38b4-111">Property value</span></span>

<span data-ttu-id="f38b4-112">Da cui ha origine l'attività.</span><span class="sxs-lookup"><span data-stu-id="f38b4-112">Where the task originated from.</span></span> <span data-ttu-id="f38b4-113">Ad esempio, da un componente, un servizio, un'applicazione o un utente.</span><span class="sxs-lookup"><span data-stu-id="f38b4-113">For example, from a component, service, application, or user.</span></span>

## <a name="remarks"></a><span data-ttu-id="f38b4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f38b4-114">Remarks</span></span>

<span data-ttu-id="f38b4-115">Durante la lettura o la scrittura di codice XML per un'attività, le informazioni sull'origine dell'attività vengono specificate utilizzando l'elemento di [**origine**](taskschedulerschema-source-registrationinfotype-element.md) dello schema di utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f38b4-115">When reading or writing XML for a task, the task source information is specified using the [**Source**](taskschedulerschema-source-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="f38b4-116">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="f38b4-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="f38b4-117">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="f38b4-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="f38b4-118">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f38b4-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="f38b4-119">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="f38b4-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f38b4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f38b4-120">Requirements</span></span>



| <span data-ttu-id="f38b4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f38b4-121">Requirement</span></span> | <span data-ttu-id="f38b4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f38b4-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38b4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f38b4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f38b4-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f38b4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f38b4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f38b4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f38b4-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f38b4-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f38b4-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f38b4-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="f38b4-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f38b4-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f38b4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f38b4-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f38b4-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f38b4-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38b4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f38b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38b4-132">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f38b4-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





