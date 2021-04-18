---
title: Funzioni Rich Edit
description: Funzioni Rich Edit
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321665"
---
# <a name="rich-edit-functions"></a><span data-ttu-id="cd6e3-103">Funzioni Rich Edit</span><span class="sxs-lookup"><span data-stu-id="cd6e3-103">Rich Edit Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cd6e3-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cd6e3-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd6e3-105">Argomento</span><span class="sxs-lookup"><span data-stu-id="cd6e3-105">Topic</span></span></th>
<th><span data-ttu-id="cd6e3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd6e3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cd6e3-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-107"><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-108">La funzione <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> è una funzione di callback definita dall'applicazione che viene utilizzata con il messaggio di <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cd6e3-108">The <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> function is an application-defined callback function that is used with the <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd6e3-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-109"><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-110">La funzione <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> è una funzione di callback definita dall'applicazione utilizzata con i messaggi <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> e <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cd6e3-110">The <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> function is an application defined callback function used with the <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> and <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> messages.</span></span> <span data-ttu-id="cd6e3-111">Viene usato per trasferire un flusso di dati all'interno o all'esterno di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-111">It is used to transfer a stream of data into or out of a rich edit control.</span></span> <span data-ttu-id="cd6e3-112">Il tipo <strong>EDITSTREAMCALLBACK</strong> definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-112">The <strong>EDITSTREAMCALLBACK</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="cd6e3-113"><em>EditStreamCallback</em> è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-113"><em>EditStreamCallback</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd6e3-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-114"><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-115">La funzione <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> è una funzione di callback definita dall'applicazione utilizzata con il messaggio di <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cd6e3-115">The <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> function is an application defined callback function used with the <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> message.</span></span> <span data-ttu-id="cd6e3-116">Determina l'indice dei caratteri della parola break o la classe di caratteri e i flag di interruzioni di parola dei caratteri nel testo specificato.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-116">It determines the character index of the word break or the character class and word-break flags of the characters in the specified text.</span></span> <span data-ttu-id="cd6e3-117">Il tipo <strong>EDITWORDBREAKPROCEX</strong> definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-117">The <strong>EDITWORDBREAKPROCEX</strong> type defines a pointer to this callback function.</span></span> <span data-ttu-id="cd6e3-118"><em>EditWordBreakProcEx</em> è un segnaposto per il nome della funzione definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-118"><em>EditWordBreakProcEx</em> is a placeholder for the application-defined function name.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd6e3-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-119"><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-120">Recupera il carattere alfanumerico Unicode UTF (Unicode Transformation Format) 32 che corrisponde al carattere BMP (Basic Multilingual Plane) specificato e allo stile matematico.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-120">Retrieves the Unicode Transformation Format (UTF)-32 math alphanumeric character that corresponds to the specified Basic Multilingual Plane (BMP) character and math style.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd6e3-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-121"><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-122">Recupera lo stile matematico e il codice carattere BMP (Basic Multilingual Plane) verticale che corrisponde al byte finale specificato di una coppia di surrogati Math.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-122">Retrieves the math style and the upright Basic Multilingual Plane (BMP) character code that corresponds to the specified trailing byte of a math surrogate pair.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd6e3-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-123"><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-124">La funzione <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> è una funzione di callback definita dall'applicazione utilizzata con il messaggio di <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cd6e3-124">The <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> function is an application defined callback function used with the <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> message.</span></span> <span data-ttu-id="cd6e3-125">Determina il modo in cui la sillabazione viene eseguita in un controllo Rich Edit di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-125">It determines how hyphenation is done in a Microsoft Rich Edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd6e3-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-126"><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-127">Converte i valori predefiniti Math, Ruby e altri oggetti inline nell'intervallo specificato in formato lineare.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-127">Translates the built-up math, ruby, and other inline objects in the specified range to linear form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd6e3-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-128"><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-129">Converte la matematica in formato lineare in un intervallo in un form predefinito oppure modifica il form predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-129">Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cd6e3-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-130"><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-131">Converte i caratteri matematici nell'intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-131">Translates the math characters in the specified range.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cd6e3-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span><span class="sxs-lookup"><span data-stu-id="cd6e3-132"><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a></span></span><br/></td>
<td><span data-ttu-id="cd6e3-133">Registra due nomi di classe, REListBox20W e RECombobox20W, che possono essere utilizzati per creare finestre ListBox o ComboBox modificate in modo completo.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-133">Registers two class names, REListBox20W and RECombobox20W, that could be used to create Rich Edit listbox or combobox windows.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cd6e3-134">Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-134">Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="cd6e3-135">Questa funzione potrebbe non essere supportata nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-135">This function may not be supported in future versions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

