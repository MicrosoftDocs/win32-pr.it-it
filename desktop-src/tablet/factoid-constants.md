---
description: Definisce valori stringa costanti usati per aumentare l'accuratezza del riconoscimento fornendo informazioni contestuali al riconoscimento.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Costanti controllo controllo (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526593"
---
# <a name="factoid-constants"></a><span data-ttu-id="95d2f-103">Costanti controllo oggetto</span><span class="sxs-lookup"><span data-stu-id="95d2f-103">Factoid Constants</span></span>

<span data-ttu-id="95d2f-104">Definisce valori stringa costanti usati per aumentare l'accuratezza del riconoscimento fornendo informazioni contestuali al riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="95d2f-104">Defines constant string values that are used to increase recognition accuracy by providing contextual information to the recognizer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="95d2f-105">Nome</span><span class="sxs-lookup"><span data-stu-id="95d2f-105">Name</span></span></th>
<th style="text-align: left;"><span data-ttu-id="95d2f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95d2f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <span data-ttu-id="95d2f-107"><dt><strong>FACTOID_NONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-107"><dt><strong>FACTOID_NONE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-108">Disabilita tutti gli altri factoids e dizionari.</span><span class="sxs-lookup"><span data-stu-id="95d2f-108">Disables all other factoids and dictionaries.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <span data-ttu-id="95d2f-109"><dt><strong>FACTOID_DEFAULT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-109"><dt> <strong>FACTOID_DEFAULT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-110">L'impostazione predefinita per factoids per le lingue occidentali include il dizionario di sistema, il dizionario utenti, le varie punteggiatura e il controllo del controllo Web e dei numeri.</span><span class="sxs-lookup"><span data-stu-id="95d2f-110">The Default setting for factoids for western languages includes the system dictionary, user dictionary, various punctuations, and the Web and Number factoid.</span></span> <span data-ttu-id="95d2f-111">L'impostazione predefinita per factoids per le lingue asiatiche orientali include tutti i caratteri supportati dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="95d2f-111">The Default setting for factoids for East Asian languages includes all characters supported by the recognizer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <span data-ttu-id="95d2f-112"><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-112"><dt> <strong>FACTOID_SYSTEMDICTIONARY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-113">Indica a un riconoscimento di utilizzare solo il dizionario di sistema.</span><span class="sxs-lookup"><span data-stu-id="95d2f-113">Indicates to a recognizer to use the system dictionary only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <span data-ttu-id="95d2f-114"><dt><strong>FACTOID_WORDLIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-114"><dt> <strong>FACTOID_WORDLIST</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-115">Indica a un riconoscimento di utilizzare un elenco di parole definito a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="95d2f-115">Indicates to a recognizer to use a programmatically-defined list of words.</span></span> <span data-ttu-id="95d2f-116">L'elenco di parole viene definito dalla proprietà <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> di un oggetto <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="95d2f-116">The list of words is defined by the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> property of a <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> object.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-117">Se una stringa viene aggiunta a un elenco di parole, anche le relative versioni in lettere maiuscole vengono aggiunte in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="95d2f-117">If a string is added to a word list, its capitalized versions are also implicitly added.</span></span> <span data-ttu-id="95d2f-118">Ad esempio, l'aggiunta di &quot; Hello &quot; aggiunge in modo implicito &quot; Hello &quot; e &quot; Hello &quot; .</span><span class="sxs-lookup"><span data-stu-id="95d2f-118">For instance, adding &quot;hello&quot; implicitly adds &quot;Hello&quot; and &quot;HELLO&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <span data-ttu-id="95d2f-119"><dt><strong>FACTOID_EMAIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-119"><dt> <strong>FACTOID_EMAIL</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-120">Indica a un riconoscimento di cercare un indirizzo di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="95d2f-120">Indicates to a recognizer to look for an email address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-121">&quot; someone@example.com &quot; Per questo controllo oggetto è necessario usare un indirizzo di posta elettronica completo, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="95d2f-121">A fully qualified email address, such as &quot;someone@example.com&quot;, must be used for this factoid.</span></span> <span data-ttu-id="95d2f-122">Un alias solitario, ad esempio un &quot; utente &quot; , non è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="95d2f-122">A lone alias, such as &quot;someone&quot;, is not recognized.</span></span>
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <span data-ttu-id="95d2f-123"><dt><strong>FACTOID_WEB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-123"><dt><strong>FACTOID_WEB</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-124">Indica a un riconoscimento di cercare un indirizzo Web.</span><span class="sxs-lookup"><span data-stu-id="95d2f-124">Indicates to a recognizer to look for a Web address.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <span data-ttu-id="95d2f-125"><dt><strong>FACTOID_ONECHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-125"><dt> <strong>FACTOID_ONECHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-126">Indica a un riconoscimento di cercare un singolo carattere.</span><span class="sxs-lookup"><span data-stu-id="95d2f-126">Indicates to a recognizer to look for a single character.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-127">Questo controllo del controllo Cerca tutti i caratteri ANSI isolati.</span><span class="sxs-lookup"><span data-stu-id="95d2f-127">This factoid looks for any isolated ANSI character.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <span data-ttu-id="95d2f-128"><dt><strong>FACTOID_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-128"><dt> <strong>FACTOID_NUMBER</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-129">Indica a un riconoscimento di cercare un numero.</span><span class="sxs-lookup"><span data-stu-id="95d2f-129">Indicates to a recognizer to look for a number.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-130">I valori numerici includono separatori, decimali, ordinali e altri simboli numerici usati comunemente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-130">Numeric values include separators, decimals, ordinals and other commonly used numeric symbols.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <span data-ttu-id="95d2f-131"><dt><strong>FACTOID_DIGIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-131"><dt> <strong>FACTOID_DIGIT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-132">Indica a un riconoscimento di cercare una singola cifra, da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="95d2f-132">Indicates to a recognizer to look for a single digit, 0 through 9.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <span data-ttu-id="95d2f-133"><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-133"><dt> <strong>FACTOID_NUMBERSIMPLE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-134">Fornisce un contesto numerico semplice a un riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="95d2f-134">Provides a simple numeric context to a recognizer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-135">Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.</span><span class="sxs-lookup"><span data-stu-id="95d2f-135">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <span data-ttu-id="95d2f-136"><dt><strong>FACTOID_CURRENCY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-136"><dt> <strong>FACTOID_CURRENCY</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-137">Indica a un riconoscimento di cercare i caratteri che identificano un valore di valuta.</span><span class="sxs-lookup"><span data-stu-id="95d2f-137">Indicates to a recognizer to look for characters that denote a currency value.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <span data-ttu-id="95d2f-138"><dt><strong>FACTOID_POSTALCODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-138"><dt> <strong>FACTOID_POSTALCODE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-139">Indica a un riconoscimento di cercare i codici postali.</span><span class="sxs-lookup"><span data-stu-id="95d2f-139">Indicates to a recognizer to look for postal codes.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <span data-ttu-id="95d2f-140"><dt><strong>FACTOID_PERCENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-140"><dt> <strong>FACTOID_PERCENT</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-141">Indica a un riconoscimento di cercare le percentuali.</span><span class="sxs-lookup"><span data-stu-id="95d2f-141">Indicates to a recognizer to look for percentages.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <span data-ttu-id="95d2f-142"><dt><strong>FACTOID_DATE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-142"><dt> <strong>FACTOID_DATE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-143">Indica a un riconoscimento di cercare i caratteri che denotano una data.</span><span class="sxs-lookup"><span data-stu-id="95d2f-143">Indicates to a recognizer to look for characters that denote a date.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <span data-ttu-id="95d2f-144"><dt><strong>FACTOID_TIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-144"><dt> <strong>FACTOID_TIME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-145">Indica a un riconoscimento di cercare i caratteri che indicano un'ora.</span><span class="sxs-lookup"><span data-stu-id="95d2f-145">Indicates to a recognizer to look for characters that denote a time.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <span data-ttu-id="95d2f-146"><dt><strong>FACTOID_TELEPHONE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-146"><dt> <strong>FACTOID_TELEPHONE</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-147">Indica a un riconoscimento di cercare i caratteri che indicano un numero di telefono.</span><span class="sxs-lookup"><span data-stu-id="95d2f-147">Indicates to a recognizer to look for characters that denote a telephone number.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <span data-ttu-id="95d2f-148"><dt><strong>FACTOID_FILENAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-148"><dt> <strong>FACTOID_FILENAME</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-149">Indica a un riconoscimento di cercare i caratteri che denotano un nome file.</span><span class="sxs-lookup"><span data-stu-id="95d2f-149">Indicates to a recognizer to look for characters that denote a file name.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <span data-ttu-id="95d2f-150"><dt><strong>FACTOID_UPPERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-150"><dt> <strong>FACTOID_UPPERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-151">Indica a un riconoscimento di cercare un singolo carattere maiuscolo: da A a Z.</span><span class="sxs-lookup"><span data-stu-id="95d2f-151">Indicates to a recognizer to look for a single uppercase character: A through Z.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <span data-ttu-id="95d2f-152"><dt><strong>FACTOID_LOWERCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-152"><dt> <strong>FACTOID_LOWERCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-153">Indica a un riconoscimento di cercare un singolo carattere minuscolo, da A A Z.</span><span class="sxs-lookup"><span data-stu-id="95d2f-153">Indicates to a recognizer to look for a single lowercase character: A through Z.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-154">Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.</span><span class="sxs-lookup"><span data-stu-id="95d2f-154">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <span data-ttu-id="95d2f-155"><dt><strong>FACTOID_PUNCCHAR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-155"><dt> <strong>FACTOID_PUNCCHAR</strong> </dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-156">Indica a un riconoscimento di cercare i caratteri di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="95d2f-156">Indicates to a recognizer to look for punctuation characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-157">Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.</span><span class="sxs-lookup"><span data-stu-id="95d2f-157">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <span data-ttu-id="95d2f-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-158"><dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-159">Indica a un riconoscimento di cercare i caratteri kanji, katakana e hiragana usati comunemente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-159">Indicates to a recognizer to look for commonly used Kanji, Katakana, and Hiragana characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <span data-ttu-id="95d2f-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-160"><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-161">Indica a un riconoscimento di cercare i caratteri in cinese semplificato usati comunemente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-161">Indicates to a recognizer to look for commonly used Simplified Chinese characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <span data-ttu-id="95d2f-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-162"><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-163">Indica a un riconoscimento di cercare i caratteri cinesi tradizionali usati comunemente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-163">Indicates to a recognizer to look for commonly used Traditional Chinese characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <span data-ttu-id="95d2f-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-164"><dt><strong>FACTOID_KOREANCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-165">Indica a un riconoscimento di cercare caratteri coreani usati comunemente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-165">Indicates to a recognizer to look for commonly used Korean characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <span data-ttu-id="95d2f-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-166"><dt><strong>FACTOID_HIRAGANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-167">Indica a un riconoscimento di cercare solo caratteri hiragana.</span><span class="sxs-lookup"><span data-stu-id="95d2f-167">Indicates to a recognizer to look for Hiragana characters only.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <span data-ttu-id="95d2f-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-168"><dt><strong>FACTOID_KATAKANA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-169">Indica a un riconoscimento di cercare solo caratteri Katakana.</span><span class="sxs-lookup"><span data-stu-id="95d2f-169">Indicates to a recognizer to look for Katakana characters only.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <span data-ttu-id="95d2f-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-170"><dt><strong>FACTOID_KANJICOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-171">Indica a un riconoscimento di cercare i caratteri kanji comunemente utilizzati.</span><span class="sxs-lookup"><span data-stu-id="95d2f-171">Indicates to a recognizer to look for commonly used kanji characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <span data-ttu-id="95d2f-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-172"><dt><strong>FACTOID_KANJIRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-173">Indica a un riconoscimento di cercare caratteri kanji usati raramente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-173">Indicates to a recognizer to look for rarely used kanji characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-174">Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.</span><span class="sxs-lookup"><span data-stu-id="95d2f-174">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <span data-ttu-id="95d2f-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-175"><dt><strong>FACTOID_BOPOMOFO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-176">Indica a un riconoscimento di cercare i caratteri Bopomofo.</span><span class="sxs-lookup"><span data-stu-id="95d2f-176">Indicates to a recognizer to look for Bopomofo characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <span data-ttu-id="95d2f-177"><dt><strong>FACTOID_JAMO</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-177"><dt><strong>FACTOID_JAMO</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-178">Indica a un riconoscitore di cercare i caratteri Jamo di compatibilità hangul.</span><span class="sxs-lookup"><span data-stu-id="95d2f-178">Indicates to a recognizer to look for Hangul compatibility Jamo characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <span data-ttu-id="95d2f-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-179"><dt><strong>FACTOID_HANGULCOMMON</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-180">Indica a un riconoscimento di cercare i caratteri hangul utilizzati comunemente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-180">Indicates to a recognizer to look for commonly used Hangul characters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <span data-ttu-id="95d2f-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="95d2f-181"><dt><strong>FACTOID_HANGULRARE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="95d2f-182">Indica a un riconoscimento di cercare i caratteri hangul utilizzati raramente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-182">Indicates to a recognizer to look for rarely used Hangul characters.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="95d2f-183">Questo controllo oggetto non è supportato in questa versione di Tablet PC SDK.</span><span class="sxs-lookup"><span data-stu-id="95d2f-183">This factoid is not supported in this version of the Tablet PC SDK.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="95d2f-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="95d2f-184">Remarks</span></span>

<span data-ttu-id="95d2f-185">In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut. h, che si trova nella <systemdrive> \\ Directory: programmi \\ Microsoft Tablet PC Platform SDK di \\ inclusione se l'SDK è stato installato nel percorso predefinito.</span><span class="sxs-lookup"><span data-stu-id="95d2f-185">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include directory if you installed the SDK in the default location.</span></span>

> [!Note]  
> <span data-ttu-id="95d2f-186">Queste costanti sono WCHAR, non BSTR.</span><span class="sxs-lookup"><span data-stu-id="95d2f-186">These constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="95d2f-187">Devono essere convertiti in BSTR prima di essere usati come parametri per i metodi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="95d2f-187">They must be converted into BSTRs before use as parameters to object methods.</span></span> <span data-ttu-id="95d2f-188">Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="95d2f-188">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="95d2f-189">Per i riconoscitori dello script latino, le factoids definite in questa classe sono fornite solo per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="95d2f-189">For recognizers of Latin script, the factoids defined in this class are provided for backward compatibility only.</span></span> <span data-ttu-id="95d2f-190">Per nuove attività di sviluppo, è consigliabile usare i valori definiti nella funzione [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) .</span><span class="sxs-lookup"><span data-stu-id="95d2f-190">For new development, you are encouraged to use the values defined in the [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) function.</span></span> <span data-ttu-id="95d2f-191">Per informazioni dettagliate, vedere [utilizzo del contesto per migliorare la precisione](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="95d2f-191">For details, see [Using Context to Improve Accuracy](using-context-to-improve-accuracy.md).</span></span>

 

<span data-ttu-id="95d2f-192">Usare questi identificatori per specificare quale controllo del controllo deve essere usato durante il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="95d2f-192">Use these identifiers to specify which factoid should be used during recognition.</span></span>

<span data-ttu-id="95d2f-193">Le seguenti combinazioni di factoids sono supportate solo per le lingue occidentali.</span><span class="sxs-lookup"><span data-stu-id="95d2f-193">The following combinations of factoids are supported for western languages only.</span></span> <span data-ttu-id="95d2f-194">Non hanno definizioni separate, ma sono input letterali stringa accettabile [**per la proprietà del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del controllo degli oggetti che usano factoids.</span><span class="sxs-lookup"><span data-stu-id="95d2f-194">These do not have separate definitions, but are acceptable string literal inputs to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of objects that use factoids.</span></span> <span data-ttu-id="95d2f-195">Queste costanti di stringa del controllore consentono all'input di trovare la corrispondenza con qualsiasi factoids nell'espressione.</span><span class="sxs-lookup"><span data-stu-id="95d2f-195">These factoid string constants allow the input to match any of the factoids in the expression.</span></span>



| <span data-ttu-id="95d2f-196">Combinazione</span><span class="sxs-lookup"><span data-stu-id="95d2f-196">Combination</span></span>               | <span data-ttu-id="95d2f-197">Definizione</span><span class="sxs-lookup"><span data-stu-id="95d2f-197">Definition</span></span>                                                |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="95d2f-198">"WEB \| wordlist"</span><span class="sxs-lookup"><span data-stu-id="95d2f-198">"WEB\|WORDLIST"</span></span>           | <span data-ttu-id="95d2f-199">Controllo Web o elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="95d2f-199">The Web factoid or the word list.</span></span>                         |
| <span data-ttu-id="95d2f-200">"messaggio di posta elettronica \| "</span><span class="sxs-lookup"><span data-stu-id="95d2f-200">"EMAIL\|WORDLIST"</span></span>         | <span data-ttu-id="95d2f-201">Il controllo dell'indirizzo di posta elettronica o l'elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="95d2f-201">The Email factoid or the word list.</span></span>                       |
| <span data-ttu-id="95d2f-202">"nome file \| Web \| "</span><span class="sxs-lookup"><span data-stu-id="95d2f-202">"FILENAME\|WEB\|WORDLIST"</span></span> | <span data-ttu-id="95d2f-203">Controllo del nome del file o controllo dell'oggetto Web o elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="95d2f-203">The Filename factoid or the Web factoid or the word list.</span></span> |



 

<span data-ttu-id="95d2f-204">Se si utilizza il controllo [InkEdit](inkedit-control-reference.md) , il controllo dell'oggetto può essere impostato come proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="95d2f-204">If you are using the [InkEdit](inkedit-control-reference.md) control, the factoid can be set as a property of the control.</span></span>

<span data-ttu-id="95d2f-205">Se si utilizzano le API della piattaforma Tablet PC, è possibile impostare la [**proprietà del controllo del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) su un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="95d2f-205">If you are using the Tablet PC Platform APIs, you can set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on an [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

<span data-ttu-id="95d2f-206">In alternativa, è possibile impostare questa proprietà con la costante della stringa del controllo dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="95d2f-206">Alternatively, you can set this property with the actual factoid string constant.</span></span>

> [!Note]  
> <span data-ttu-id="95d2f-207">Le costanti di stringa del controllo del controllo sono maiuscole.</span><span class="sxs-lookup"><span data-stu-id="95d2f-207">Factoid string constants are case sensitive.</span></span> <span data-ttu-id="95d2f-208">Per altre informazioni su factoids e su come usarle, vedere uso del contesto per [migliorare la precisione](using-context-to-improve-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="95d2f-208">For more information about factoids and how to use them, see Using Context to [Improve Accuracy](using-context-to-improve-accuracy.md).</span></span> <span data-ttu-id="95d2f-209">Per determinare se un controllo del controllo è disponibile in una lingua specifica, vedere [Supported Factoids dalla versione 1](supported-factoids-from-version-1.md).</span><span class="sxs-lookup"><span data-stu-id="95d2f-209">To determine whether a factoid is available in a specific language, see [Supported Factoids from Version 1](supported-factoids-from-version-1.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95d2f-210">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95d2f-210">Requirements</span></span>



| <span data-ttu-id="95d2f-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d2f-211">Requirement</span></span> | <span data-ttu-id="95d2f-212">Valore</span><span class="sxs-lookup"><span data-stu-id="95d2f-212">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d2f-213">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d2f-213">Minimum supported client</span></span><br/> | <span data-ttu-id="95d2f-214">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="95d2f-214">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="95d2f-215">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d2f-215">Minimum supported server</span></span><br/> | <span data-ttu-id="95d2f-216">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="95d2f-216">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="95d2f-217">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95d2f-217">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d2f-218"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="95d2f-218"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95d2f-219">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95d2f-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="95d2f-220">[**Classe InkRecognizeContext proprietà di controllo \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="95d2f-220">[**Factoid Property \[InkRecognizeContext Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="95d2f-221">[**Proprietà del controllo del controllo della \[ Classe PenInputPanel\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="95d2f-221">[**Factoid Property \[PenInputPanel Class\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)</span></span>
</dt> <dt>

<span data-ttu-id="95d2f-222">[**Controllo proprietà \[ controllo InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span><span class="sxs-lookup"><span data-stu-id="95d2f-222">[**Factoid Property \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)</span></span>
</dt> <dt>

[<span data-ttu-id="95d2f-223">Uso del contesto per migliorare l'accuratezza</span><span class="sxs-lookup"><span data-stu-id="95d2f-223">Using Context to Improve Accuracy</span></span>](using-context-to-improve-accuracy.md)
</dt> <dt>

[<span data-ttu-id="95d2f-224">Factoids supportati dalla versione 1</span><span class="sxs-lookup"><span data-stu-id="95d2f-224">Supported Factoids from Version 1</span></span>](supported-factoids-from-version-1.md)
</dt> </dl>

 

