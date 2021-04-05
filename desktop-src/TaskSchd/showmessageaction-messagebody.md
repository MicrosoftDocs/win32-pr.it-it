---
title: Proprietà ShowMessageAction. MessageBody
description: Per lo scripting, ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Utilità di pianificazione proprietà MessageBody
- Utilità di pianificazione proprietà MessageBody, oggetto ShowMessageAction
- Oggetto ShowMessageAction Utilità di pianificazione, Proprietà MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873489"
---
# <a name="showmessageactionmessagebody-property"></a><span data-ttu-id="932f3-106">Proprietà ShowMessageAction. MessageBody</span><span class="sxs-lookup"><span data-stu-id="932f3-106">ShowMessageAction.MessageBody property</span></span>

<span data-ttu-id="932f3-107">\[Questo oggetto non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="932f3-107">\[This object is no longer supported.</span></span> <span data-ttu-id="932f3-108">È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.\]</span><span class="sxs-lookup"><span data-stu-id="932f3-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="932f3-109">Per lo scripting, ottiene o imposta il testo del messaggio visualizzato nel corpo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="932f3-109">For scripting, gets or sets the message text that is displayed in the body of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="932f3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="932f3-110">Syntax</span></span>


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a><span data-ttu-id="932f3-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="932f3-111">Property value</span></span>

<span data-ttu-id="932f3-112">Testo del messaggio visualizzato nel corpo della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="932f3-112">The message text that is displayed in the body of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="932f3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="932f3-113">Remarks</span></span>

<span data-ttu-id="932f3-114">Le stringhe con parametri possono essere utilizzate nel testo del messaggio della finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="932f3-114">Parameterized strings can be used in the message text of the message box.</span></span> <span data-ttu-id="932f3-115">Per ulteriori informazioni, vedere la sezione Esempi in [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="932f3-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="932f3-116">Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="932f3-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="932f3-117">Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse.</span><span class="sxs-lookup"><span data-stu-id="932f3-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="932f3-118">Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="932f3-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="932f3-119">Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="932f3-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="932f3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="932f3-120">Requirements</span></span>



| <span data-ttu-id="932f3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="932f3-121">Requirement</span></span> | <span data-ttu-id="932f3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="932f3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="932f3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="932f3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="932f3-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="932f3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="932f3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="932f3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="932f3-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="932f3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="932f3-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="932f3-127">End of client support</span></span><br/>    | <span data-ttu-id="932f3-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="932f3-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="932f3-129">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="932f3-129">End of server support</span></span><br/>    | <span data-ttu-id="932f3-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="932f3-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="932f3-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="932f3-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="932f3-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="932f3-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="932f3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="932f3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="932f3-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="932f3-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="932f3-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="932f3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="932f3-136">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="932f3-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

