---
description: In questa sezione vengono descritte le funzioni di gestione delle stringhe della shell di Windows. Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.
title: Funzioni di gestione delle stringhe della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c2e47785db10ba7dc4bbe54e78e3a06be1b152a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968336"
---
# <a name="shell-string-handling-functions"></a><span data-ttu-id="fdec1-104">Funzioni di gestione delle stringhe della shell</span><span class="sxs-lookup"><span data-stu-id="fdec1-104">Shell String Handling Functions</span></span>

<span data-ttu-id="fdec1-105">In questa sezione vengono descritte le funzioni di gestione delle stringhe della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="fdec1-105">This section describes the Windows Shell string handling functions.</span></span> <span data-ttu-id="fdec1-106">Gli elementi di programmazione descritti in questa documentazione vengono esportati da Shlwapi.dll e definiti in Shlwapi. h e Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="fdec1-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fdec1-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="fdec1-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fdec1-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="fdec1-108">Topic</span></span></th>
<th><span data-ttu-id="fdec1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdec1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fdec1-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-111">Esegue un confronto tra due caratteri.</span><span class="sxs-lookup"><span data-stu-id="fdec1-111">Performs a comparison between two characters.</span></span> <span data-ttu-id="fdec1-112">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-112">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-113"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-114">Recupera una stringa utilizzata con i siti Web quando si specificano le preferenze della lingua.</span><span class="sxs-lookup"><span data-stu-id="fdec1-114">Retrieves a string used with websites when specifying language preferences.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-116">Esegue un confronto con distinzione tra maiuscole e minuscole di un numero specificato di caratteri dall'inizio di due stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="fdec1-116">Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-117"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-118">Esegue un confronto senza distinzione tra maiuscole e minuscole di un numero specificato di caratteri dall'inizio di due stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="fdec1-118">Performs a case-insensitive comparison of a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-120">Confronta un numero specificato di caratteri dall'inizio di due stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="fdec1-120">Compares a specified number of characters from the beginning of two localized strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-121"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-122">Determina se un carattere rappresenta uno spazio.</span><span class="sxs-lookup"><span data-stu-id="fdec1-122">Determines whether a character represents a space.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-124">Estrae una risorsa di testo specificata quando la risorsa viene specificata sotto forma di stringa indiretta (una stringa che inizia con il simbolo ' @').</span><span class="sxs-lookup"><span data-stu-id="fdec1-124">Extracts a specified text resource when given that resource in the form of an indirect string (a string that begins with the '@' symbol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-126">Crea una copia di una stringa nella memoria appena allocata.</span><span class="sxs-lookup"><span data-stu-id="fdec1-126">Makes a copy of a string in newly allocated memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-128">Accoda una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="fdec1-128">Appends one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-129">Non usare.</span><span class="sxs-lookup"><span data-stu-id="fdec1-129">Do not use.</span></span> <span data-ttu-id="fdec1-130">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-130">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-132">Copia e aggiunge caratteri da una stringa alla fine di un altro.</span><span class="sxs-lookup"><span data-stu-id="fdec1-132">Copies and appends characters from one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-133">Non usare.</span><span class="sxs-lookup"><span data-stu-id="fdec1-133">Do not use.</span></span> <span data-ttu-id="fdec1-134">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-134">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-135"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-136">Concatena due stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="fdec1-136">Concatenates two Unicode strings.</span></span> <span data-ttu-id="fdec1-137">Utilizzato quando sono necessarie concatenazioni ripetute allo stesso buffer.</span><span class="sxs-lookup"><span data-stu-id="fdec1-137">Used when repeated concatenations to the same buffer are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-139">Cerca in una stringa la prima occorrenza di un carattere che corrisponde al carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-139">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="fdec1-140">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-140">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-141"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-142">Cerca in una stringa la prima occorrenza di un carattere che corrisponde al carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-142">Searches a string for the first occurrence of a character that matches the specified character.</span></span> <span data-ttu-id="fdec1-143">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-143">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-145">Cerca in una stringa la prima occorrenza di un carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-145">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="fdec1-146">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-146">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-147"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-148">Cerca in una stringa la prima occorrenza di un carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-148">Searches a string for the first occurrence of a specified character.</span></span> <span data-ttu-id="fdec1-149">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-149">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-151">Confronta due stringhe per determinare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fdec1-151">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="fdec1-152">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-152">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-153"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-154">Confronta le stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fdec1-154">Compares strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fdec1-155">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-155">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-157">Confronta due stringhe per determinare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fdec1-157">Compares two strings to determine if they are the same.</span></span> <span data-ttu-id="fdec1-158">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-158">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-159"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-160">Confronta due stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fdec1-160">Compares two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fdec1-161">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-161">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-162"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-163">Confronta due stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="fdec1-163">Compares two Unicode strings.</span></span> <span data-ttu-id="fdec1-164">Le cifre nelle stringhe vengono considerate come contenuti numerici anziché come testo.</span><span class="sxs-lookup"><span data-stu-id="fdec1-164">Digits in the strings are considered as numerical content rather than text.</span></span> <span data-ttu-id="fdec1-165">Questo test non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-165">This test is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-167">Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fdec1-167">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="fdec1-168">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-168">The comparison is case-sensitive.</span></span> <span data-ttu-id="fdec1-169">La macro <strong>StrNCmp</strong> è diversa da questa funzione solo nel nome.</span><span class="sxs-lookup"><span data-stu-id="fdec1-169">The <strong>StrNCmp</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-170"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-171">Confronta un numero specificato di caratteri dall'inizio di due stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fdec1-171">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fdec1-172">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-172">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-173"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-174">Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fdec1-174">Compares a specified number of characters from the beginning of two strings to determine if they are the same.</span></span> <span data-ttu-id="fdec1-175">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-175">The comparison is not case-sensitive.</span></span> <span data-ttu-id="fdec1-176">La macro <strong>StrNCmpI</strong> è diversa da questa funzione solo nel nome.</span><span class="sxs-lookup"><span data-stu-id="fdec1-176">The <strong>StrNCmpI</strong> macro differs from this function in name only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-177"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-178">Confronta un numero specificato di caratteri dall'inizio di due stringhe utilizzando le regole di confronto della fase di esecuzione del linguaggio C (ASCII).</span><span class="sxs-lookup"><span data-stu-id="fdec1-178">Compares a specified number of characters from the beginning of two strings using C run-time (ASCII) collation rules.</span></span> <span data-ttu-id="fdec1-179">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-179">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-180"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-181">Copia una stringa in un'altra.</span><span class="sxs-lookup"><span data-stu-id="fdec1-181">Copies one string to another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-182">Non usare.</span><span class="sxs-lookup"><span data-stu-id="fdec1-182">Do not use.</span></span> <span data-ttu-id="fdec1-183">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-183">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-184"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-185">Copia un numero specificato di caratteri dall'inizio di una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="fdec1-185">Copies a specified number of characters from the beginning of one string to another.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-186">Non usare questa funzione o la macro <strong>StrNCpy</strong> .</span><span class="sxs-lookup"><span data-stu-id="fdec1-186">Do not use this function or the <strong>StrNCpy</strong> macro.</span></span> <span data-ttu-id="fdec1-187">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-187">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-188"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-189">Cerca in una stringa la prima occorrenza di un gruppo di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fdec1-189">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="fdec1-190">Il metodo di ricerca fa distinzione tra maiuscole e minuscole e il carattere <strong>null</strong> di terminazione è incluso nella corrispondenza dei criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fdec1-190">The search method is case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-191"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-192">Cerca in una stringa la prima occorrenza di un gruppo di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fdec1-192">Searches a string for the first occurrence of any of a group of characters.</span></span> <span data-ttu-id="fdec1-193">Il metodo di ricerca non fa distinzione tra maiuscole e minuscole e il carattere di terminazione <strong>null</strong> è incluso nella corrispondenza dei criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fdec1-193">The search method is not case-sensitive, and the terminating <strong>NULL</strong> character is included within the search pattern match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-195">Duplica una stringa.</span><span class="sxs-lookup"><span data-stu-id="fdec1-195">Duplicates a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-197">Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fdec1-197">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-199">Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fdec1-199">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="fdec1-200">Differisce da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in un tipo di parametro.</span><span class="sxs-lookup"><span data-stu-id="fdec1-200">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-201"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-202">Converte un valore numerico in una stringa che rappresenta il numero in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fdec1-202">Converts a numeric value into a string that represents the number in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="fdec1-203">Estende <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> offrendo l'opzione per arrotondare alla cifra visualizzata più vicina o per eliminare le cifre non visualizzate.</span><span class="sxs-lookup"><span data-stu-id="fdec1-203">Extends <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> by offering the option to round to the nearest displayed digit or to discard undisplayed digits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-205">Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in byte, kilobyte, megabyte o gigabyte, a seconda delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fdec1-205">Converts a numeric value into a string that represents the number expressed as a size value in bytes, kilobytes, megabytes, or gigabytes, depending on the size.</span></span> <span data-ttu-id="fdec1-206">Differisce da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in un tipo di parametro.</span><span class="sxs-lookup"><span data-stu-id="fdec1-206">Differs from <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> in one parameter type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-207"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-208">Converte un valore numerico in una stringa che rappresenta il numero espresso come valore di dimensione in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="fdec1-208">Converts a numeric value into a string that represents the number expressed as a size value in kilobytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-209"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-210">Converte un intervallo di tempo, in millisecondi, in una stringa.</span><span class="sxs-lookup"><span data-stu-id="fdec1-210">Converts a time interval, specified in milliseconds, to a string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-212">Confronta un numero specificato di caratteri dall'inizio di due stringhe per determinare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="fdec1-212">Compares a specified number of characters from the beginning of two strings to determine if they are equal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-214">Accoda un numero specificato di caratteri dall'inizio di una stringa alla fine di un altro.</span><span class="sxs-lookup"><span data-stu-id="fdec1-214">Appends a specified number of characters from the beginning of one string to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-215">Non usare questa funzione o la macro <strong>StrCatN</strong> .</span><span class="sxs-lookup"><span data-stu-id="fdec1-215">Do not use this function or the <strong>StrCatN</strong> macro.</span></span> <span data-ttu-id="fdec1-216">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-216">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-217"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-218">Cerca in una stringa la prima occorrenza di un carattere contenuto in un buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-218">Searches a string for the first occurrence of a character contained in a specified buffer.</span></span> <span data-ttu-id="fdec1-219">Questa ricerca non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="fdec1-219">This search does not include the terminating null character.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-220"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-221">Cerca in una stringa l'ultima occorrenza di un carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-221">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="fdec1-222">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-222">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-223"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-224">Cerca in una stringa l'ultima occorrenza di un carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-224">Searches a string for the last occurrence of a specified character.</span></span> <span data-ttu-id="fdec1-225">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-225">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-226"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-227">Accetta una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> che contiene o punta a una stringa e restituisce tale stringa come <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fdec1-227">Accepts a <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> that contains or points to a string, and returns that string as a <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-228"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-229">Converte una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> in una stringa e inserisce il risultato in un buffer.</span><span class="sxs-lookup"><span data-stu-id="fdec1-229">Converts an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-230"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-231">Accetta una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e restituisce un puntatore a una stringa allocata contenente il nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-231">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a> and returns a pointer to an allocated string containing the display name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-232"><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-233">Accetta una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> restituita da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a>, la converte in una stringa e inserisce il risultato in un buffer.</span><span class="sxs-lookup"><span data-stu-id="fdec1-233">Takes an <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> structure returned by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder::GetDisplayNameOf</strong></a>, converts it to a string, and places the result in a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-235">Consente di cercare l'ultima occorrenza di una sottostringa specificata all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="fdec1-235">Searches for the last occurrence of a specified substring within a string.</span></span> <span data-ttu-id="fdec1-236">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-236">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-237"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-238">Ottiene la lunghezza di una sottostringa all'interno di una stringa costituita interamente da caratteri contenuti in un buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="fdec1-238">Obtains the length of a substring within a string that consists entirely of characters contained in a specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-239"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-240">Trova la prima occorrenza di una sottostringa all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="fdec1-240">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="fdec1-241">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-241">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-243">Trova la prima occorrenza di una sottostringa all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="fdec1-243">Finds the first occurrence of a substring within a string.</span></span> <span data-ttu-id="fdec1-244">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fdec1-244">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-245"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-246">Converte una stringa che rappresenta un valore decimale in un intero.</span><span class="sxs-lookup"><span data-stu-id="fdec1-246">Converts a string that represents a decimal value to an integer.</span></span> <span data-ttu-id="fdec1-247">La macro <strong>StrToLong</strong> è identica a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fdec1-247">The <strong>StrToLong</strong> macro is identical to this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-249">Converte una stringa che rappresenta un valore decimale o esadecimale in un intero a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="fdec1-249">Converts a string representing a decimal or hexadecimal value to a 64-bit integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-251">Converte una stringa che rappresenta un numero decimale o esadecimale in un valore integer.</span><span class="sxs-lookup"><span data-stu-id="fdec1-251">Converts a string representing a decimal or hexadecimal number to an integer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-252"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-253">Rimuove i caratteri iniziali e finali specificati da una stringa.</span><span class="sxs-lookup"><span data-stu-id="fdec1-253">Removes specified leading and trailing characters from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fdec1-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-254"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-255">Accetta un elenco di argomenti a lunghezza variabile e restituisce i valori degli argomenti come stringa formattata in stile <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fdec1-255">Takes a variable-length argument list and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-256">Non usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fdec1-256">Do not use this function.</span></span> <span data-ttu-id="fdec1-257">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-257">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fdec1-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="fdec1-258"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a></span></span><br/></td>
<td><span data-ttu-id="fdec1-259">Accetta un elenco di argomenti e restituisce i valori degli argomenti come stringa formattata in stile <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fdec1-259">Takes a list of arguments and returns the values of the arguments as a <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>-style formatted string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fdec1-260">Non usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fdec1-260">Do not use this function.</span></span> <span data-ttu-id="fdec1-261">Vedere la sezione Osservazioni per le funzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="fdec1-261">See Remarks for alternative functions.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
