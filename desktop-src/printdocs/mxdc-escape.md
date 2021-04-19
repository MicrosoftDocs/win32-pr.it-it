---
description: La \_ funzione di escape della stampante MXDC Escape consente alle applicazioni di scrivere documenti in un file o in una stampante in formato XPS (XML Paper Specification) per mezzo di Microsoft XPS Document Converter (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: Funzione MXDC_ESCAPE (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 08b5ae7e44f7b9c35d6a395b78ce514aee050e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311820"
---
# <a name="mxdc_escape-function"></a><span data-ttu-id="505a2-103">MXDC \_ escape-funzione</span><span class="sxs-lookup"><span data-stu-id="505a2-103">MXDC\_ESCAPE function</span></span>

<span data-ttu-id="505a2-104">La funzione di escape della stampante **MXDC \_ escape** consente alle applicazioni di scrivere documenti in un file o in una stampante in formato XPS (XML Paper Specification) per mezzo di Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="505a2-104">The **MXDC\_ESCAPE** printer escape function enables applications to write documents to a file or to a printer in XML Paper Specification (XPS) format by means of the Microsoft XPS Document Converter (MXDC).</span></span>

<span data-ttu-id="505a2-105">Per eseguire questa operazione, chiamare la funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="505a2-105">To perform this operation, call the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function with the following parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="505a2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="505a2-106">Syntax</span></span>


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a><span data-ttu-id="505a2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="505a2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="505a2-108">*HDC*</span><span class="sxs-lookup"><span data-stu-id="505a2-108">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="505a2-109">Handle per il contesto di dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="505a2-109">A handle to the printer device context.</span></span>

</dd> <dt>

<span data-ttu-id="505a2-110">*cbInput*</span><span class="sxs-lookup"><span data-stu-id="505a2-110">*cbInput*</span></span> 
</dt> <dd>

<span data-ttu-id="505a2-111">Dimensione, in byte, dei dati a cui punta il parametro *lpszInData* .</span><span class="sxs-lookup"><span data-stu-id="505a2-111">The size, in bytes, of the data pointed to by the *lpszInData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="505a2-112">*lpszInData*</span><span class="sxs-lookup"><span data-stu-id="505a2-112">*lpszInData*</span></span> 
</dt> <dd>

<span data-ttu-id="505a2-113">Puntatore a un buffer contenente i dati di input, che vengono sempre archiviati in una delle seguenti strutture.</span><span class="sxs-lookup"><span data-stu-id="505a2-113">A pointer to a buffer containing the input data, which is always stored in one of the following structures.</span></span>

<dl> <dd><span data-ttu-id="505a2-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span><span class="sxs-lookup"><span data-stu-id="505a2-114"><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></span></span></dd> <dd><span data-ttu-id="505a2-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span><span class="sxs-lookup"><span data-stu-id="505a2-115"><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></span></span></dd> <dd><span data-ttu-id="505a2-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span><span class="sxs-lookup"><span data-stu-id="505a2-116"><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></span></span></dd> <dd><span data-ttu-id="505a2-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span><span class="sxs-lookup"><span data-stu-id="505a2-117"><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></span></span></dd> </dl>

<span data-ttu-id="505a2-118">Ognuna di queste strutture dispone di un membro opcode che specifica le operazioni che MXDC deve eseguire.</span><span class="sxs-lookup"><span data-stu-id="505a2-118">Each of these structures has an opcode member that specifies what the MXDC is supposed to do.</span></span> <span data-ttu-id="505a2-119">Per osservazioni dettagliate su questi codici, vedere MxdcEscapeHeader.</span><span class="sxs-lookup"><span data-stu-id="505a2-119">See MxdcEscapeHeader for detailed remarks about these codes.</span></span>



| <span data-ttu-id="505a2-120">Codice operativo</span><span class="sxs-lookup"><span data-stu-id="505a2-120">Operations code (opcode)</span></span>                                                                                                                                                                                                  | <span data-ttu-id="505a2-121">Azione</span><span class="sxs-lookup"><span data-stu-id="505a2-121">Action</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <span data-ttu-id="505a2-122"><dt>**MXDCOP \_ ottenere il \_ nome file**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-122"><dt>**MXDCOP\_GET\_FILENAME**</dt></span></span> </dl>                                          | <span data-ttu-id="505a2-123">Imposta il parametro *lpszOutData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) su, ovvero il percorso completo del file di output come stringa con terminazione zero oppure la dimensione di tale stringa.</span><span class="sxs-lookup"><span data-stu-id="505a2-123">Sets the *lpszOutData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function to, either the full path of the output file as a zero-terminated string or else the size of that string.</span></span><br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <span data-ttu-id="505a2-124"><dt>**MXDCOP \_ \_ documento fisso di PRINTTICKET \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-124"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**</dt></span></span> </dl> | <span data-ttu-id="505a2-125">Associa un ticket di stampa a una sequenza di documenti fissa XPS.</span><span class="sxs-lookup"><span data-stu-id="505a2-125">Associates a print ticket with an XPS fixed document sequence.</span></span><br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <span data-ttu-id="505a2-126"><dt>**\_ \_ doc fisso PRINTTICKET \_ MXDCOP**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-126"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_DOC**</dt></span></span> </dl>              | <span data-ttu-id="505a2-127">Associa un ticket di stampa a un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="505a2-127">Associates a print ticket with an XPS document.</span></span><br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <span data-ttu-id="505a2-128"><dt>**\_ \_ pagina fissa PRINTTICKET \_ MXDCOP**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-128"><dt>**MXDCOP\_PRINTTICKET\_FIXED\_PAGE**</dt></span></span> </dl>           | <span data-ttu-id="505a2-129">Associa un ticket di stampa a una pagina XPS.</span><span class="sxs-lookup"><span data-stu-id="505a2-129">Associates a print ticket with an XPS page.</span></span><br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <span data-ttu-id="505a2-130"><dt>**MXDCOP \_ set \_ S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-130"><dt>**MXDCOP\_SET\_S0PAGE**</dt></span></span> </dl>                                                | <span data-ttu-id="505a2-131">Invia il markup XPS della pagina corrente all'output.</span><span class="sxs-lookup"><span data-stu-id="505a2-131">Sends the XPS markup of the current page to the output.</span></span><br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <span data-ttu-id="505a2-132"><dt>**MXDCOP \_ impostare \_ la \_ risorsa S0PAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-132"><dt>**MXDCOP\_SET\_S0PAGE\_RESOURCE**</dt></span></span> </dl>                    | <span data-ttu-id="505a2-133">Invia all'output una risorsa nella pagina, ad esempio un'immagine o un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="505a2-133">Sends a resource on the page, such as an image or font, to the output.</span></span><br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <span data-ttu-id="505a2-134"><dt>**MXDCOP \_ impostare \_ la \_ modalità XPSPASSTHRU**</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-134"><dt>**MXDCOP\_SET\_XPSPASSTHRU\_MODE**</dt></span></span> </dl>                 | <span data-ttu-id="505a2-135">Inserisce il MXDC in uno stato di pass-through, consentendo a un'applicazione di scrivere XPS direttamente nel file di output senza alcuna elaborazione da parte di MXDC.</span><span class="sxs-lookup"><span data-stu-id="505a2-135">Puts the MXDC into a pass through state, enabling an application to write XPS directly to the output file without any processing by the MXDC.</span></span> <span data-ttu-id="505a2-136">In questo modo è possibile scrivere un intero documento o persino una sequenza di documenti.</span><span class="sxs-lookup"><span data-stu-id="505a2-136">An entire document or even document sequence can be written in this way.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="505a2-137">*cbOutput*</span><span class="sxs-lookup"><span data-stu-id="505a2-137">*cbOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="505a2-138">Dimensione, in byte, dei dati a cui punta il parametro *lpszOutData* .</span><span class="sxs-lookup"><span data-stu-id="505a2-138">The size, in bytes, of the data pointed to by the *lpszOutData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="505a2-139">*lpszOutData*</span><span class="sxs-lookup"><span data-stu-id="505a2-139">*lpszOutData*</span></span> 
</dt> <dd>

<span data-ttu-id="505a2-140">Puntatore a un buffer contenente i dati di output.</span><span class="sxs-lookup"><span data-stu-id="505a2-140">A pointer to a buffer containing the output data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="505a2-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="505a2-141">Return value</span></span>

<span data-ttu-id="505a2-142">Se la funzione ha esito positivo, il valore restituito è maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="505a2-142">If the function succeeds, the return value is greater than zero.</span></span> <span data-ttu-id="505a2-143">Se la funzione ha esito negativo o non è supportata, il valore restituito è minore o uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="505a2-143">If the function fails or is not supported, the return value is less than or equal to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="505a2-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="505a2-144">Remarks</span></span>

<span data-ttu-id="505a2-145">Questo escape è supportato da MXDC e XPSDrv, ma non da GDI.</span><span class="sxs-lookup"><span data-stu-id="505a2-145">This escape is supported by MXDC and XPSDrv, but not by GDI.</span></span>

<span data-ttu-id="505a2-146">Per determinare se il driver della stampante è MXDC, chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con l'escape [**GetTechnology**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="505a2-146">To determine if the printer driver is the MXDC, call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) escape.</span></span> <span data-ttu-id="505a2-147">Se il driver è MXDC, **ExtEscape** restituirà la stringa con terminazione zero " http://schemas.microsoft.com/xps/2005/06 ".</span><span class="sxs-lookup"><span data-stu-id="505a2-147">If the driver is the MXDC, the **ExtEscape** will return the zero-terminated string, "http://schemas.microsoft.com/xps/2005/06".</span></span> <span data-ttu-id="505a2-148">Verificare che il buffer a cui fa riferimento il parametro *lpszOutData* sia sufficientemente grande da contenere questa stringa.</span><span class="sxs-lookup"><span data-stu-id="505a2-148">Be sure the buffer referenced by the *lpszOutData* parameter is large enough to hold this string.</span></span>

<span data-ttu-id="505a2-149">Per determinare se il driver della stampante è il driver Microsoft XPS Document Writer di Windows, verificare che il driver della stampante sia MXDC, quindi determinare se il nome del driver della stampante è "Microsoft XPS Document Writer".</span><span class="sxs-lookup"><span data-stu-id="505a2-149">To determine if the printer driver is the Windows in-box Microsoft XPS Document Writer driver, confirm that the printer driver is the MXDC, and then determine whether the name of the printer driver is "Microsoft XPS Document Writer".</span></span>

<span data-ttu-id="505a2-150">Per ottenere il nome del driver della stampante, utilizzare una delle tecniche seguenti.</span><span class="sxs-lookup"><span data-stu-id="505a2-150">To get the printer driver name, use one of the following techniques.</span></span> <dl> <span data-ttu-id="505a2-151">Chiamare [**GetPrinterDriver**](getprinterdriver.md) con il valore del parametro *Level* impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="505a2-151">Call [**GetPrinterDriver**](getprinterdriver.md) with the *Level* parameter value set to 1.</span></span> <span data-ttu-id="505a2-152">Il nome del driver della stampante viene restituito nel membro **pname** della struttura di [**informazioni sul driver \_ \_ 1**](driver-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="505a2-152">The printer driver name is returned in the **pName** member of the [**DRIVER\_INFO\_1**](driver-info-1.md) structure.</span></span>  
<span data-ttu-id="505a2-153">oppure</span><span class="sxs-lookup"><span data-stu-id="505a2-153">or</span></span>  
<span data-ttu-id="505a2-154">Chiamare [**GetPrinter**](getprinter.md) con il valore del parametro *Level* impostato su 2.</span><span class="sxs-lookup"><span data-stu-id="505a2-154">Call [**GetPrinter**](getprinter.md) with the *Level* parameter value set to 2.</span></span> <span data-ttu-id="505a2-155">Il nome del driver della stampante viene restituito nel membro **pDriverName** della struttura [**Printer \_ info \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="505a2-155">The printer driver name is returned in the **pDriverName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>  
</dl>

<span data-ttu-id="505a2-156">Nella tabella seguente viene illustrato dove trovare vari oggetti nel file XPS. verranno scritti i vari tipi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="505a2-156">The following table shows where to find various objects in the XPS file various types of objects will be written.</span></span>



| <span data-ttu-id="505a2-157">Oggetto</span><span class="sxs-lookup"><span data-stu-id="505a2-157">Object</span></span>       | <span data-ttu-id="505a2-158">Posizione nel file di output</span><span class="sxs-lookup"><span data-stu-id="505a2-158">Location in the output file</span></span>    |
|--------------|--------------------------------|
| <span data-ttu-id="505a2-159">Pagina fissa</span><span class="sxs-lookup"><span data-stu-id="505a2-159">Fixed Page</span></span>   | <span data-ttu-id="505a2-160">/Documents/1/Pages/Esc%d.fpage</span><span class="sxs-lookup"><span data-stu-id="505a2-160">/Documents/1/Pages/Esc%d.fpage</span></span> |
| <span data-ttu-id="505a2-161">Anteprima</span><span class="sxs-lookup"><span data-stu-id="505a2-161">Thumbnail</span></span>    | <span data-ttu-id="505a2-162">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="505a2-162">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="505a2-163">Stampa ticket</span><span class="sxs-lookup"><span data-stu-id="505a2-163">Print Ticket</span></span> | <span data-ttu-id="505a2-164">/Documents/1/Metadata</span><span class="sxs-lookup"><span data-stu-id="505a2-164">/Documents/1/Metadata</span></span>          |
| <span data-ttu-id="505a2-165">Carattere</span><span class="sxs-lookup"><span data-stu-id="505a2-165">Font</span></span>         | <span data-ttu-id="505a2-166">/Documents/1/Resources/Fonts</span><span class="sxs-lookup"><span data-stu-id="505a2-166">/Documents/1/Resources/Fonts</span></span>   |
| <span data-ttu-id="505a2-167">Immagine</span><span class="sxs-lookup"><span data-stu-id="505a2-167">Image</span></span>        | <span data-ttu-id="505a2-168">/Documents/1/Resources/Images</span><span class="sxs-lookup"><span data-stu-id="505a2-168">/Documents/1/Resources/Images</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="505a2-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="505a2-169">Requirements</span></span>



| <span data-ttu-id="505a2-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="505a2-170">Requirement</span></span> | <span data-ttu-id="505a2-171">Valore</span><span class="sxs-lookup"><span data-stu-id="505a2-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="505a2-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="505a2-172">Minimum supported client</span></span><br/> | <span data-ttu-id="505a2-173">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="505a2-173">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="505a2-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="505a2-174">Minimum supported server</span></span><br/> | <span data-ttu-id="505a2-175">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="505a2-175">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="505a2-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="505a2-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="505a2-177"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="505a2-177"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="505a2-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="505a2-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="505a2-179">Stampa</span><span class="sxs-lookup"><span data-stu-id="505a2-179">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

<span data-ttu-id="505a2-180">[Funzioni di escape della stampante](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="505a2-180">[Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="505a2-181">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="505a2-181">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

