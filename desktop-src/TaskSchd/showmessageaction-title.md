---
title: Proprietà ShowMessageAction. title
description: Per lo scripting, ottiene o imposta il titolo della finestra di messaggio.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Utilità di pianificazione proprietà titolo
- Utilità di pianificazione proprietà titolo, oggetto ShowMessageAction
- Oggetto ShowMessageAction Utilità di pianificazione, proprietà title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740602"
---
# <a name="showmessageactiontitle-property"></a><span data-ttu-id="e31f5-106">Proprietà ShowMessageAction. title</span><span class="sxs-lookup"><span data-stu-id="e31f5-106">ShowMessageAction.Title property</span></span>

<span data-ttu-id="e31f5-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="e31f5-107">\[This object is no longer supported.</span></span> <span data-ttu-id="e31f5-108">È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]</span><span class="sxs-lookup"><span data-stu-id="e31f5-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="e31f5-109">Per lo scripting, ottiene o imposta il titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e31f5-109">For scripting, gets or sets the title of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31f5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e31f5-110">Syntax</span></span>


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a><span data-ttu-id="e31f5-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e31f5-111">Property value</span></span>

<span data-ttu-id="e31f5-112">Titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e31f5-112">The title of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31f5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e31f5-113">Remarks</span></span>

<span data-ttu-id="e31f5-114">Le stringhe con parametri possono essere utilizzate nel testo del titolo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="e31f5-114">Parameterized strings can be used in the title text of the message box.</span></span> <span data-ttu-id="e31f5-115">Per ulteriori informazioni, vedere la sezione Esempi in [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="e31f5-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="e31f5-116">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="e31f5-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="e31f5-117">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="e31f5-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="e31f5-118">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e31f5-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="e31f5-119">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="e31f5-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31f5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e31f5-120">Requirements</span></span>



| <span data-ttu-id="e31f5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31f5-121">Requirement</span></span> | <span data-ttu-id="e31f5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e31f5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e31f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e31f5-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e31f5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e31f5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e31f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e31f5-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e31f5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e31f5-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e31f5-127">End of client support</span></span><br/>    | <span data-ttu-id="e31f5-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e31f5-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e31f5-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e31f5-129">End of server support</span></span><br/>    | <span data-ttu-id="e31f5-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e31f5-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e31f5-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e31f5-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="e31f5-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e31f5-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e31f5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e31f5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31f5-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31f5-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31f5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e31f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31f5-136">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="e31f5-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

