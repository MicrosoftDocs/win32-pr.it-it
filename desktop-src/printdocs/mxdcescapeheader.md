---
description: La struttura MXDC dell' \_ \_ intestazione \_ di escape T include il codice operativo per una chiamata a ExtEscape con MXDC \_ escape come parametro nEscape. Fornisce anche le dimensioni dei buffer di input e di output.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: Struttura MXDC_ESCAPE_HEADER_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885173"
---
# <a name="mxdc_escape_header_t-structure"></a><span data-ttu-id="5acbd-104">\_ \_ Struttura T dell'intestazione di escape MXDC \_</span><span class="sxs-lookup"><span data-stu-id="5acbd-104">MXDC\_ESCAPE\_HEADER\_T structure</span></span>

<span data-ttu-id="5acbd-105">La struttura **MXDC dell' \_ intestazione di escape \_ \_ T** include il codice operativo per una chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ escape**](mxdc-escape.md) come parametro *nEscape* .</span><span class="sxs-lookup"><span data-stu-id="5acbd-105">The **MXDC\_ESCAPE\_HEADER\_T** structure holds the operation code for a call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with [**MXDC\_ESCAPE**](mxdc-escape.md) as the *nEscape* parameter.</span></span> <span data-ttu-id="5acbd-106">Fornisce anche le dimensioni dei buffer di input e di output.</span><span class="sxs-lookup"><span data-stu-id="5acbd-106">It also provides the sizes of the input and output buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5acbd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5acbd-107">Syntax</span></span>


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a><span data-ttu-id="5acbd-108">Members</span><span class="sxs-lookup"><span data-stu-id="5acbd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5acbd-109">**cbInput**</span><span class="sxs-lookup"><span data-stu-id="5acbd-109">**cbInput**</span></span>
</dt> <dd>

<span data-ttu-id="5acbd-110">Dimensioni del buffer di input che verranno passate al parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-110">The size of the input buffer that will be passed to the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="5acbd-111">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="5acbd-111">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="5acbd-112">Dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="5acbd-112">The size of the output buffer.</span></span> <span data-ttu-id="5acbd-113">Si tratta dello stesso valore del parametro *cbOutput* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-113">This is the same value as the *cbOutput* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function.</span></span>

</dd> <dt>

<span data-ttu-id="5acbd-114">**Codice operativo**</span><span class="sxs-lookup"><span data-stu-id="5acbd-114">**opCode**</span></span>
</dt> <dd>

<span data-ttu-id="5acbd-115">Costante del codice che indica a MXDC cosa fare.</span><span class="sxs-lookup"><span data-stu-id="5acbd-115">The code constant that tells MXDC what to do.</span></span>



| <span data-ttu-id="5acbd-116">Codice operativo</span><span class="sxs-lookup"><span data-stu-id="5acbd-116">Operations code</span></span>                      | <span data-ttu-id="5acbd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5acbd-117">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5acbd-118">MXDCOP \_ ottenere il \_ nome file</span><span class="sxs-lookup"><span data-stu-id="5acbd-118">MXDCOP\_GET\_FILENAME</span></span>                | <span data-ttu-id="5acbd-119">Restituisce, nel parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , il percorso completo del file di output come stringa con terminazione zero o la dimensione di tale stringa.</span><span class="sxs-lookup"><span data-stu-id="5acbd-119">Returns, in the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function, either the full path of the output file as a zero-terminated string or the size of that string.</span></span> <span data-ttu-id="5acbd-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5acbd-120">See Remarks.</span></span>                   |
| <span data-ttu-id="5acbd-121">MXDCOP \_ \_ documento fisso di PRINTTICKET \_ \_</span><span class="sxs-lookup"><span data-stu-id="5acbd-121">MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ</span></span> | <span data-ttu-id="5acbd-122">Associa un ticket di stampa a una sequenza di documenti fissa XPS.</span><span class="sxs-lookup"><span data-stu-id="5acbd-122">Associates a print ticket with an XPS fixed document sequence.</span></span>                                                                                                                                                         |
| <span data-ttu-id="5acbd-123">\_ \_ doc fisso PRINTTICKET \_ MXDCOP</span><span class="sxs-lookup"><span data-stu-id="5acbd-123">MXDCOP\_PRINTTICKET\_FIXED\_DOC</span></span>      | <span data-ttu-id="5acbd-124">Associa un ticket di stampa a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="5acbd-124">Associates a print ticket with an XPS document.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="5acbd-125">\_ \_ pagina fissa PRINTTICKET \_ MXDCOP</span><span class="sxs-lookup"><span data-stu-id="5acbd-125">MXDCOP\_PRINTTICKET\_FIXED\_PAGE</span></span>     | <span data-ttu-id="5acbd-126">Associa un ticket di stampa a una pagina XPS.</span><span class="sxs-lookup"><span data-stu-id="5acbd-126">Associates a print ticket with an XPS page.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="5acbd-127">MXDCOP \_ set \_ S0PAGE</span><span class="sxs-lookup"><span data-stu-id="5acbd-127">MXDCOP\_SET\_S0PAGE</span></span>                  | <span data-ttu-id="5acbd-128">Invia il markup XPS della pagina corrente all'output.</span><span class="sxs-lookup"><span data-stu-id="5acbd-128">Sends the XPS markup of the current page to the output.</span></span>                                                                                                                                                                |
| <span data-ttu-id="5acbd-129">MXDCOP \_ impostare \_ la \_ risorsa S0PAGE</span><span class="sxs-lookup"><span data-stu-id="5acbd-129">MXDCOP\_SET\_S0PAGE\_RESOURCE</span></span>        | <span data-ttu-id="5acbd-130">Invia all'output una risorsa nella pagina, ad esempio un'immagine o un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5acbd-130">Sends a resource on the page, such as an image or font, to the output.</span></span>                                                                                                                                                 |
| <span data-ttu-id="5acbd-131">MXDCOP \_ impostare \_ la \_ modalità XPSPASSTHRU</span><span class="sxs-lookup"><span data-stu-id="5acbd-131">MXDCOP\_SET\_XPSPASSTHRU\_MODE</span></span>       | <span data-ttu-id="5acbd-132">Inserisce il MXDC in uno stato pass-through, consentendo a un'applicazione di scrivere XPS direttamente nel file di output senza alcuna elaborazione da parte di MXDC.</span><span class="sxs-lookup"><span data-stu-id="5acbd-132">Puts the MXDC into a pass-through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="5acbd-133">In questo modo è possibile scrivere un intero documento o persino una sequenza di documenti.</span><span class="sxs-lookup"><span data-stu-id="5acbd-133">An entire document or even document sequence can be written in this way.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5acbd-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="5acbd-134">Remarks</span></span>

<span data-ttu-id="5acbd-135">Prima di chiamare [**MXDC \_ escape**](mxdc-escape.md), le \_ applicazioni devono prima verificare che il driver sia MXDC chiamando [**EXTESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con l'escape [**GetTechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-135">Before calling [**MXDC\_ESCAPE**](mxdc-escape.md),\_applications should first verify that the driver is MXDC by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="5acbd-136">Se il driver è MXDC, la funzione restituisce la stringa con terminazione zero " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="5acbd-136">If the driver is the MXDC the function returns the zero-terminated string "http://schemas.microsoft.com/xps/2005/06".</span></span>

<span data-ttu-id="5acbd-137">Questa struttura è sempre all'inizio dei dati passati alla funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) nel parametro *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="5acbd-137">This structure is always at the beginning of the data passed to the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function in its *lpszInData* parameter.</span></span>

<span data-ttu-id="5acbd-138">Quando **OpCode** è MXDCOP \_ get \_ FileName:</span><span class="sxs-lookup"><span data-stu-id="5acbd-138">When **opCode** is MXDCOP\_GET\_FILENAME:</span></span>

-   <span data-ttu-id="5acbd-139">Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito solo dall' **\_ \_ intestazione \_ T di escape MXDC** .</span><span class="sxs-lookup"><span data-stu-id="5acbd-139">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="5acbd-140">Ottenere il nome del file di output chiamando [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) due volte.</span><span class="sxs-lookup"><span data-stu-id="5acbd-140">Obtain the output filename by calling [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) twice.</span></span>
    1.  <span data-ttu-id="5acbd-141">La prima volta, passare 4 al parametro *cbOutput* di [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="5acbd-141">The first time, pass 4 to the *cbOutput* parameter of [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="5acbd-142">Impostare il parametro *lpszOutData* in modo che punti a tutti i 4 byte allocati di memoria.</span><span class="sxs-lookup"><span data-stu-id="5acbd-142">Set the *lpszOutData* parameter to point to any allocated 4 bytes of memory.</span></span> <span data-ttu-id="5acbd-143">La dimensione del percorso completo del file verrà restituita nel parametro *lpszOutData* di **ExtEscape**.</span><span class="sxs-lookup"><span data-stu-id="5acbd-143">The size of the fully qualified file path will be returned in the *lpszOutData* parameter of **ExtEscape**.</span></span>
    2.  <span data-ttu-id="5acbd-144">Chiamare quindi di nuovo la funzione.</span><span class="sxs-lookup"><span data-stu-id="5acbd-144">Then call the function again.</span></span> <span data-ttu-id="5acbd-145">Questa volta imposta sia *cbOutput* che *cbInput* su 4 + *DataSize*.</span><span class="sxs-lookup"><span data-stu-id="5acbd-145">This time set both *cbOutput* and *cbInput* to 4+ *DataSize*.</span></span> <span data-ttu-id="5acbd-146">Il percorso completo del file verrà restituito in una struttura [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-146">The fully qualified file path will be returned in an [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) structure.</span></span>

<span data-ttu-id="5acbd-147">Quando **OpCode** è MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq o MXDCOP \_ PrintTicket \_ fixed \_ doc:</span><span class="sxs-lookup"><span data-stu-id="5acbd-147">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ or MXDCOP\_PRINTTICKET\_FIXED\_DOC:</span></span>

-   <span data-ttu-id="5acbd-148">Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenata in una struttura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-148">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="5acbd-149">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="5acbd-149">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

<span data-ttu-id="5acbd-150">Quando **OpCode** è MXDCOP \_ PRINTTICKET \_ fixed \_ Page:</span><span class="sxs-lookup"><span data-stu-id="5acbd-150">When **opCode** is MXDCOP\_PRINTTICKET\_FIXED\_PAGE:</span></span>

-   <span data-ttu-id="5acbd-151">Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenata in una struttura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-151">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) structure concatenated into an [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) structure.</span></span>
-   <span data-ttu-id="5acbd-152">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="5acbd-152">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="5acbd-153">Quando **OpCode** è MXDCOP \_ set \_ S0PAGE:</span><span class="sxs-lookup"><span data-stu-id="5acbd-153">When **opCode** is MXDCOP\_SET\_S0PAGE:</span></span>

-   <span data-ttu-id="5acbd-154">Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenata in una struttura [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-154">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcS0PageData**](mxdcs0pagedata.md) structure concatenated into an [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) structure.</span></span>
-   <span data-ttu-id="5acbd-155">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="5acbd-155">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>
-   <span data-ttu-id="5acbd-156">L'applicazione chiamante è responsabile della convalida del codice XML.</span><span class="sxs-lookup"><span data-stu-id="5acbd-156">The calling application is responsible for validating the XML.</span></span>
-   <span data-ttu-id="5acbd-157">Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ impostare \_ \_ la risorsa S0PAGE come **OpCode** per ogni risorsa nella pagina prima di chiamarla con MXDCOP \_ set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="5acbd-157">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="5acbd-158">Quando **OpCode** è MXDCOP \_ set \_ S0PAGE \_ Resource:</span><span class="sxs-lookup"><span data-stu-id="5acbd-158">When **opCode** is MXDCOP\_SET\_S0PAGE\_RESOURCE:</span></span>

-   <span data-ttu-id="5acbd-159">Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito dalla **struttura \_ \_ \_ T dell'intestazione di escape MXDC** e da una struttura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenata in una struttura [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="5acbd-159">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of the **MXDC\_ESCAPE\_HEADER\_T** structure and an [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) structure concatenated into an [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) structure.</span></span>
-   <span data-ttu-id="5acbd-160">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), ma possono essere presenti più chiamate tra le chiamate a **Startpage** e **EndPage** .</span><span class="sxs-lookup"><span data-stu-id="5acbd-160">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), but there can be multiple such calls between the **StartPage** and **EndPage** calls.</span></span>
-   <span data-ttu-id="5acbd-161">Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ impostare \_ \_ la risorsa S0PAGE come **OpCode** per ogni risorsa nella pagina prima di chiamarla con MXDCOP \_ set \_ S0PAGE.</span><span class="sxs-lookup"><span data-stu-id="5acbd-161">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with MXDCOP\_SET\_S0PAGE\_RESOURCE as **opCode** for each resource on the page before you call it with MXDCOP\_SET\_S0PAGE.</span></span>

<span data-ttu-id="5acbd-162">Quando **OpCode** è MXDCOP \_ set \_ XPSPASSTHRU \_ mode:</span><span class="sxs-lookup"><span data-stu-id="5acbd-162">When **opCode** is MXDCOP\_SET\_XPSPASSTHRU\_MODE:</span></span>

-   <span data-ttu-id="5acbd-163">Il parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) è costituito solo dall' **\_ \_ intestazione \_ T di escape MXDC** .</span><span class="sxs-lookup"><span data-stu-id="5acbd-163">The *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function consists of only the **MXDC\_ESCAPE\_HEADER\_T** structure.</span></span>
-   <span data-ttu-id="5acbd-164">Questa chiamata deve essere eseguita prima della chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span><span class="sxs-lookup"><span data-stu-id="5acbd-164">This call must occur before the call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).</span></span>

## <a name="requirements"></a><span data-ttu-id="5acbd-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5acbd-165">Requirements</span></span>



| <span data-ttu-id="5acbd-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="5acbd-166">Requirement</span></span> | <span data-ttu-id="5acbd-167">Valore</span><span class="sxs-lookup"><span data-stu-id="5acbd-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5acbd-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5acbd-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5acbd-169">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5acbd-169">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5acbd-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5acbd-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5acbd-171">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5acbd-171">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5acbd-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5acbd-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="5acbd-173"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="5acbd-173"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5acbd-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5acbd-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acbd-175">Stampa</span><span class="sxs-lookup"><span data-stu-id="5acbd-175">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5acbd-176">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="5acbd-176">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="5acbd-177">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5acbd-177">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5acbd-178">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="5acbd-178">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="5acbd-179">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="5acbd-179">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

