---
title: Messaggio di WM_DDE_EXECUTE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di esecuzione DDE di WM a un'applicazione server DDE per inviare una stringa al server da elaborare come una serie di comandi.
ms.assetid: 23c18a57-83ee-4fd3-a5bc-71645bda34eb
keywords:
- Scambio di dati del messaggio WM_DDE_EXECUTE
topic_type:
- apiref
api_name:
- WM_DDE_EXECUTE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957b5cadcd2383d535aa67258725bafff57ab4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400687"
---
# <a name="wm_dde_execute-message"></a><span data-ttu-id="09e83-104">\_Messaggio di \_ esecuzione DDE WM</span><span class="sxs-lookup"><span data-stu-id="09e83-104">WM\_DDE\_EXECUTE message</span></span>

<span data-ttu-id="09e83-105">Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di **\_ \_ esecuzione DDE di WM** a un'applicazione server DDE per inviare una stringa al server da elaborare come una serie di comandi.</span><span class="sxs-lookup"><span data-stu-id="09e83-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_EXECUTE** message to a DDE server application to send a string to the server to be processed as a series of commands.</span></span> <span data-ttu-id="09e83-106">Si prevede che l'applicazione server invii un [**messaggio \_ \_ ACK DDE WM**](wm-dde-ack.md) in risposta.</span><span class="sxs-lookup"><span data-stu-id="09e83-106">The server application is expected to post a [**WM\_DDE\_ACK**](wm-dde-ack.md) message in response.</span></span>

<span data-ttu-id="09e83-107">Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="09e83-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_EXECUTE     0x03E8
```



## <a name="parameters"></a><span data-ttu-id="09e83-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="09e83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e83-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09e83-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09e83-110">Handle per la finestra client che invia il messaggio.</span><span class="sxs-lookup"><span data-stu-id="09e83-110">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="09e83-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09e83-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09e83-112">Contiene un oggetto memoria globale che fa riferimento a una stringa di comando ANSI o Unicode, a seconda dei tipi di Windows necessari per la conversazione.</span><span class="sxs-lookup"><span data-stu-id="09e83-112">Contains a global memory object that references an ANSI or Unicode command string, depending on the types of windows involved in the conversation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09e83-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="09e83-113">Remarks</span></span>

<span data-ttu-id="09e83-114">La stringa di comando è una stringa con terminazione null costituita da una o più stringhe opcode racchiuse tra parentesi quadre ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="09e83-114">The command string is a null-terminated string consisting of one or more opcode strings enclosed in single brackets (\[ \]).</span></span> <span data-ttu-id="09e83-115">Ogni stringa opcode presenta la sintassi seguente, in cui l'elenco *Parameters* è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="09e83-115">Each opcode string has the following syntax, where the *parameters* list is optional:</span></span>

<span data-ttu-id="09e83-116">*parametri OpCode*</span><span class="sxs-lookup"><span data-stu-id="09e83-116">*opcode parameters*</span></span>

<span data-ttu-id="09e83-117">Il *codice operativo* è qualsiasi singolo token definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09e83-117">The *opcode* is any application-defined single token.</span></span> <span data-ttu-id="09e83-118">Non può includere spazi, virgole, parentesi, parentesi quadre o virgolette.</span><span class="sxs-lookup"><span data-stu-id="09e83-118">It cannot include spaces, commas, parentheses, brackets, or quotation marks.</span></span>

<span data-ttu-id="09e83-119">L'elenco *Parameters* può contenere qualsiasi valore o valore definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="09e83-119">The *parameters* list can contain any application-defined value or values.</span></span> <span data-ttu-id="09e83-120">Più parametri sono separati da virgole e l'intero elenco di parametri è racchiuso tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="09e83-120">Multiple parameters are separated by commas, and the entire parameter list is enclosed in parentheses.</span></span> <span data-ttu-id="09e83-121">I parametri non possono includere virgole o parentesi tranne che all'interno di una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="09e83-121">Parameters cannot include commas or parentheses except inside a quoted string.</span></span> <span data-ttu-id="09e83-122">Se un carattere tra parentesi quadre o parentesi deve essere visualizzato in una stringa racchiusa tra virgolette, non è necessario raddoppiarlo, come nel caso delle regole precedenti.</span><span class="sxs-lookup"><span data-stu-id="09e83-122">If a bracket or parenthesis character is to appear in a quoted string, it need not be doubled, as was the case under the old rules.</span></span>

<span data-ttu-id="09e83-123">Di seguito sono riportate stringhe di comando valide:</span><span class="sxs-lookup"><span data-stu-id="09e83-123">The following are valid command strings:</span></span>


```
[connect][download(query1,results.txt)][disconnect] 
[query("sales per employee for each district")] 
[open("sample.xlm")][run("r1c1")] 
[quote_case("This is a "" character")] 
[bracket_or_paren_case("()s or []s should be no problem.")] 
```



<span data-ttu-id="09e83-124">Si noti che, in base alle regole precedenti, le parentesi e le parentesi quadre devono essere raddoppiate, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="09e83-124">Note that, under the old rules, parentheses and brackets had to be doubled, as follows:</span></span>


```
[bracket_or_paren_case("(())s or [[]]s should be no problem.")] 
```



<span data-ttu-id="09e83-125">I server devono essere in grado di analizzare i comandi in entrambi i moduli.</span><span class="sxs-lookup"><span data-stu-id="09e83-125">Servers should be able to parse commands in either form.</span></span>

<span data-ttu-id="09e83-126">Le stringhe di esecuzione Unicode devono essere utilizzate solo quando entrambe le finestre client e server gestiscono la funzione [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="09e83-126">Unicode execute strings should be used only when both the client and server window handles cause the [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) function to return **TRUE**.</span></span>

### <a name="posting"></a><span data-ttu-id="09e83-127">Distacco</span><span class="sxs-lookup"><span data-stu-id="09e83-127">Posting</span></span>

<span data-ttu-id="09e83-128">L'applicazione client alloca l'oggetto memoria globale chiamando la funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="09e83-128">The client application allocates the global memory object by calling the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span>

<span data-ttu-id="09e83-129">Quando si elabora il messaggio [**\_ \_ ACK di WM DDE**](wm-dde-ack.md) che il server invia come risposta a un messaggio di **\_ \_ esecuzione DDE WM** , l'applicazione client deve eliminare l'oggetto restituito dal messaggio **\_ \_ ACK DDE WM** .</span><span class="sxs-lookup"><span data-stu-id="09e83-129">When processing the [**WM\_DDE\_ACK**](wm-dde-ack.md) message that the server posts in reply to a **WM\_DDE\_EXECUTE** message, the client application must delete the object returned by the **WM\_DDE\_ACK** message.</span></span>

### <a name="receiving"></a><span data-ttu-id="09e83-130">Ricezione</span><span class="sxs-lookup"><span data-stu-id="09e83-130">Receiving</span></span>

<span data-ttu-id="09e83-131">L'applicazione server inserisce il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="09e83-131">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="09e83-132">Il server deve riutilizzare l'oggetto memoria globale.</span><span class="sxs-lookup"><span data-stu-id="09e83-132">The server should reuse the global memory object.</span></span>

<span data-ttu-id="09e83-133">Se non specificato diversamente da un sottoprotocollo, il server non deve inserire il messaggio [**\_ \_ ACK DDE di WM**](wm-dde-ack.md) finché non vengono completate tutte le azioni specificate dalla stringa di comando Execute.</span><span class="sxs-lookup"><span data-stu-id="09e83-133">Unless specified otherwise by a sub-protocol, the server should not post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message until all the actions specified by the execute command string are completed.</span></span> <span data-ttu-id="09e83-134">L'unica eccezione a questa regola è rappresentata dal caso in cui la stringa causa la terminazione della conversazione da parte del server.</span><span class="sxs-lookup"><span data-stu-id="09e83-134">The one exception to this rule is when the string causes the server to terminate the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e83-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09e83-135">Requirements</span></span>



| <span data-ttu-id="09e83-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e83-136">Requirement</span></span> | <span data-ttu-id="09e83-137">Valore</span><span class="sxs-lookup"><span data-stu-id="09e83-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e83-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e83-138">Minimum supported client</span></span><br/> | <span data-ttu-id="09e83-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09e83-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="09e83-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e83-140">Minimum supported server</span></span><br/> | <span data-ttu-id="09e83-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="09e83-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="09e83-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09e83-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e83-143"><dt>DDE. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09e83-143"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e83-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09e83-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="09e83-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="09e83-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="09e83-146">**IsWindowUnicode**</span><span class="sxs-lookup"><span data-stu-id="09e83-146">**IsWindowUnicode**</span></span>](/windows/desktop/api/winuser/nf-winuser-iswindowunicode)
</dt> <dt>

[<span data-ttu-id="09e83-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="09e83-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="09e83-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="09e83-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="09e83-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="09e83-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="09e83-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="09e83-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="09e83-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="09e83-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="09e83-152">**\_ACK DDE \_ WM**</span><span class="sxs-lookup"><span data-stu-id="09e83-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="09e83-153">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="09e83-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="09e83-154">Informazioni su Dynamic Data Exchange</span><span class="sxs-lookup"><span data-stu-id="09e83-154">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

