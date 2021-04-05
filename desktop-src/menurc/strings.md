---
title: Stringhe
description: In questa sezione vengono illustrate le funzioni di stringa.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- risorse, stringhe
- stringhe
- funzioni per i valori stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3231006de2dfe6ed611b58e5b511819a40c21e8b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732098"
---
# <a name="strings"></a><span data-ttu-id="faf80-106">Stringhe</span><span class="sxs-lookup"><span data-stu-id="faf80-106">Strings</span></span>

<span data-ttu-id="faf80-107">Questa sezione descrive le funzioni di stringa e spiega come usarle nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="faf80-107">This section describes the string functions and explains how to use them in your applications.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="faf80-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="faf80-108">In This Section</span></span>



| <span data-ttu-id="faf80-109">Nome</span><span class="sxs-lookup"><span data-stu-id="faf80-109">Name</span></span>                                     | <span data-ttu-id="faf80-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faf80-110">Description</span></span>                                             |
|------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="faf80-111">Informazioni sulle stringhe</span><span class="sxs-lookup"><span data-stu-id="faf80-111">About Strings</span></span>](about-strings.md)       | <span data-ttu-id="faf80-112">Vengono illustrate le funzioni di stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-112">Discusses the string functions.</span></span><br/>              |
| [<span data-ttu-id="faf80-113">Informazioni su strsafe. h</span><span class="sxs-lookup"><span data-stu-id="faf80-113">About Strsafe.h</span></span>](strsafe-ovw.md)       | <span data-ttu-id="faf80-114">Vengono illustrate le funzioni di stringa in strsafe. h.</span><span class="sxs-lookup"><span data-stu-id="faf80-114">Discusses the string functions in Strsafe.h.</span></span><br/> |
| [<span data-ttu-id="faf80-115">Riferimento alla stringa</span><span class="sxs-lookup"><span data-stu-id="faf80-115">String Reference</span></span>](string-reference.md) | <span data-ttu-id="faf80-116">Contiene il riferimento all'API.</span><span class="sxs-lookup"><span data-stu-id="faf80-116">Contains the API reference.</span></span><br/>                  |



 

### <a name="string-functions"></a><span data-ttu-id="faf80-117">Funzioni di stringa</span><span class="sxs-lookup"><span data-stu-id="faf80-117">String Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faf80-118">Nome</span><span class="sxs-lookup"><span data-stu-id="faf80-118">Name</span></span></th>
<th><span data-ttu-id="faf80-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faf80-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="faf80-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-120"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a></span></span></td>
<td><span data-ttu-id="faf80-121">Converte una stringa di caratteri o un singolo carattere in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="faf80-121">Converts a character string or a single character to lowercase.</span></span> <span data-ttu-id="faf80-122">Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto.</span><span class="sxs-lookup"><span data-stu-id="faf80-122">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-123"><a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a></span></span></td>
<td><span data-ttu-id="faf80-124">Converte i caratteri maiuscoli in un buffer in caratteri minuscoli.</span><span class="sxs-lookup"><span data-stu-id="faf80-124">Converts uppercase characters in a buffer to lowercase characters.</span></span> <span data-ttu-id="faf80-125">La funzione converte i caratteri sul posto.</span><span class="sxs-lookup"><span data-stu-id="faf80-125">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-126"><a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a></span></span></td>
<td><span data-ttu-id="faf80-127">Recupera un puntatore al carattere successivo in una stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-127">Retrieves a pointer to the next character in a string.</span></span> <span data-ttu-id="faf80-128">Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.</span><span class="sxs-lookup"><span data-stu-id="faf80-128">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-129"><a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a></span></span></td>
<td><span data-ttu-id="faf80-130">Recupera il puntatore al carattere successivo in una stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-130">Retrieves the pointer to the next character in a string.</span></span> <span data-ttu-id="faf80-131">Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.</span><span class="sxs-lookup"><span data-stu-id="faf80-131">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-132"><a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a></span></span></td>
<td><span data-ttu-id="faf80-133">Recupera un puntatore al carattere precedente in una stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-133">Retrieves a pointer to the preceding character in a string.</span></span> <span data-ttu-id="faf80-134">Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.</span><span class="sxs-lookup"><span data-stu-id="faf80-134">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-135"><a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a></span></span></td>
<td><span data-ttu-id="faf80-136">Recupera il puntatore al carattere precedente in una stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-136">Retrieves the pointer to the preceding character in a string.</span></span> <span data-ttu-id="faf80-137">Questa funzione può gestire le stringhe costituite da caratteri a byte singolo o multibyte.</span><span class="sxs-lookup"><span data-stu-id="faf80-137">This function can handle strings consisting of either single- or multi-byte characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-138"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a></span></span></td>
<td><span data-ttu-id="faf80-139">Converte una stringa nel set di caratteri definito dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="faf80-139">Translates a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-140"><a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a></span></span></td>
<td><span data-ttu-id="faf80-141">Converte un numero specificato di caratteri in una stringa nel set di caratteri definito dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="faf80-141">Translates a specified number of characters in a string into the OEM-defined character set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-142"><a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a></span></span></td>
<td><span data-ttu-id="faf80-143">Converte una stringa di caratteri o un singolo carattere in maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="faf80-143">Converts a character string or a single character to uppercase.</span></span> <span data-ttu-id="faf80-144">Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto.</span><span class="sxs-lookup"><span data-stu-id="faf80-144">If the operand is a character string, the function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-145"><a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a></span></span></td>
<td><span data-ttu-id="faf80-146">Converte i caratteri minuscoli di un buffer in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="faf80-146">Converts lowercase characters in a buffer to uppercase characters.</span></span> <span data-ttu-id="faf80-147">La funzione converte i caratteri sul posto.</span><span class="sxs-lookup"><span data-stu-id="faf80-147">The function converts the characters in place.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-148"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a></span></span></td>
<td><span data-ttu-id="faf80-149">Confronta due stringhe di caratteri, usando le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="faf80-149">Compares two character strings, using the specified locale.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="faf80-150">Per compatibilità con Unicode, usare <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> o la versione Unicode di <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="faf80-150">For compatibility with Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> or the Unicode version of <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-151"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a></span></span></td>
<td><span data-ttu-id="faf80-152">Confronta due stringhe Unicode (caratteri wide), usando le impostazioni locali specificate.</span><span class="sxs-lookup"><span data-stu-id="faf80-152">Compares two Unicode (wide character) strings, using the specified locale.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>Della funzione FoldString</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-153"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a></span></span></td>
<td><span data-ttu-id="faf80-154">Esegue il mapping di una stringa a un'altra, eseguendo un'opzione di trasformazione specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-154">Maps one string to another, performing a specified transformation option.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-155"><a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a></span></span></td>
<td><span data-ttu-id="faf80-156">Recupera le informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-156">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="faf80-157">Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output.</span><span class="sxs-lookup"><span data-stu-id="faf80-157">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="faf80-158">Ogni bit identifica un tipo di carattere specificato, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.</span><span class="sxs-lookup"><span data-stu-id="faf80-158">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-159"><a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a></span></span></td>
<td><span data-ttu-id="faf80-160">Recupera le informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-160">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="faf80-161">Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output.</span><span class="sxs-lookup"><span data-stu-id="faf80-161">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="faf80-162">Ogni bit identifica un tipo di carattere specificato, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.</span><span class="sxs-lookup"><span data-stu-id="faf80-162">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span> <br/> <span data-ttu-id="faf80-163">A differenza dei parenti di chiusura <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> e <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> presenta il comportamento standard tramite l'uso dell'opzione <strong> # define Unicode</strong> .</span><span class="sxs-lookup"><span data-stu-id="faf80-163">Unlike its close relatives <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> and <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>, <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> exhibits standard behavior through the use of the <strong>#define UNICODE</strong> switch.</span></span> <span data-ttu-id="faf80-164">Si tratta della funzione consigliata.</span><span class="sxs-lookup"><span data-stu-id="faf80-164">It is the recommended function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-165"><a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a></span></span></td>
<td><span data-ttu-id="faf80-166">Recupera le informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-166">Retrieves character-type information for the characters in the specified source string.</span></span> <span data-ttu-id="faf80-167">Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output.</span><span class="sxs-lookup"><span data-stu-id="faf80-167">For each character in the string, the function sets one or more bits in the corresponding 16-bit element of the output array.</span></span> <span data-ttu-id="faf80-168">Ogni bit identifica un tipo di carattere specificato, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.</span><span class="sxs-lookup"><span data-stu-id="faf80-168">Each bit identifies a given character type, such as whether the character is a letter, a digit, or neither.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-169"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a></span></span></td>
<td><span data-ttu-id="faf80-170">Determina se un carattere è un carattere alfabetico.</span><span class="sxs-lookup"><span data-stu-id="faf80-170">Determines whether a character is an alphabetical character.</span></span> <span data-ttu-id="faf80-171">Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="faf80-171">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-172"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a></span></span></td>
<td><span data-ttu-id="faf80-173">Determina se un carattere è un carattere alfabetico o numerico.</span><span class="sxs-lookup"><span data-stu-id="faf80-173">Determines whether a character is either an alphabetical or a numeric character.</span></span> <span data-ttu-id="faf80-174">Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="faf80-174">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-175"><a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a></span></span></td>
<td><span data-ttu-id="faf80-176">Determina se un carattere è minuscolo.</span><span class="sxs-lookup"><span data-stu-id="faf80-176">Determines whether a character is lowercase.</span></span> <span data-ttu-id="faf80-177">Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="faf80-177">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-178"><a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a></span></span></td>
<td><span data-ttu-id="faf80-179">Determina se un carattere è in maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="faf80-179">Determines whether a character is uppercase.</span></span> <span data-ttu-id="faf80-180">Questa determinazione è basata sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="faf80-180">This determination is based on the semantics of the language selected by the user during setup or through Control Panel.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-181"><a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a></span></span></td>
<td><span data-ttu-id="faf80-182">Carica una risorsa di tipo stringa dal file eseguibile associato a un modulo specificato, copia la stringa in un buffer e aggiunge un carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="faf80-182">Loads a string resource from the executable file associated with a specified module, copies the string into a buffer, and appends a terminating NULL character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-183"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a></span></span></td>
<td><span data-ttu-id="faf80-184">Accoda una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-184">Appends one string to another.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>LSTRCMP</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-185"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a></span></span></td>
<td><span data-ttu-id="faf80-186">Confronta due stringhe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="faf80-186">Compares two character strings.</span></span> <span data-ttu-id="faf80-187">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="faf80-187">The comparison is case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>due</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-188"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a></span></span></td>
<td><span data-ttu-id="faf80-189">Confronta due stringhe di caratteri.</span><span class="sxs-lookup"><span data-stu-id="faf80-189">Compares two character strings.</span></span> <span data-ttu-id="faf80-190">Nel confronto non viene fatta distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="faf80-190">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-191"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a></span></span></td>
<td><span data-ttu-id="faf80-192">Copia una stringa in un buffer.</span><span class="sxs-lookup"><span data-stu-id="faf80-192">Copies a string to a buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-193"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a></span></span></td>
<td><span data-ttu-id="faf80-194">Copia un numero specificato di caratteri da una stringa di origine in un buffer.</span><span class="sxs-lookup"><span data-stu-id="faf80-194">Copies a specified number of characters from a source string into a buffer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-195"><a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a></span></span></td>
<td><span data-ttu-id="faf80-196">Determina la lunghezza della stringa specificata (escluso il carattere null di terminazione).</span><span class="sxs-lookup"><span data-stu-id="faf80-196">Determines the length of the specified string (not including the terminating null character).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-197"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a></span></span></td>
<td><span data-ttu-id="faf80-198">Converte una stringa dal set di caratteri definito dall'OEM in una stringa ANSI o a caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="faf80-198">Translates a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-199"><a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a></span></span></td>
<td><span data-ttu-id="faf80-200">Converte un numero specificato di caratteri in una stringa dal set di caratteri definito dall'OEM in una stringa ANSI o di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="faf80-200">Translates a specified number of characters in a string from the OEM-defined character set into either an ANSI or a wide-character string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="faf80-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-201"><a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a></span></span></td>
<td><span data-ttu-id="faf80-202">Scrive i dati formattati nel buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="faf80-202">Writes formatted data to the specified buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="faf80-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span><span class="sxs-lookup"><span data-stu-id="faf80-203"><a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a></span></span></td>
<td><span data-ttu-id="faf80-204">Scrive i dati formattati nel buffer specificato utilizzando un puntatore a un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="faf80-204">Writes formatted data to the specified buffer using a pointer to a list of arguments.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="strsafe-functions"></a><span data-ttu-id="faf80-205">Funzioni strsafe</span><span class="sxs-lookup"><span data-stu-id="faf80-205">Strsafe Functions</span></span>



| <span data-ttu-id="faf80-206">Nome</span><span class="sxs-lookup"><span data-stu-id="faf80-206">Name</span></span>                                             | <span data-ttu-id="faf80-207">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faf80-207">Description</span></span>                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="faf80-208">**StringCbCat**</span><span class="sxs-lookup"><span data-stu-id="faf80-208">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | <span data-ttu-id="faf80-209">Concatena una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-209">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="faf80-210">**StringCbCatEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-210">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | <span data-ttu-id="faf80-211">Concatena una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-211">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="faf80-212">**StringCbCatN**</span><span class="sxs-lookup"><span data-stu-id="faf80-212">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | <span data-ttu-id="faf80-213">Concatena il numero specificato di byte da una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-213">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="faf80-214">**StringCbCatNEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-214">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | <span data-ttu-id="faf80-215">Concatena il numero specificato di byte da una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-215">Concatenates the specified number of bytes from one string to another string.</span></span><br/>         |
| [<span data-ttu-id="faf80-216">**StringCbCopy**</span><span class="sxs-lookup"><span data-stu-id="faf80-216">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | <span data-ttu-id="faf80-217">Copia una stringa in un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-217">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="faf80-218">**StringCbCopyEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-218">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | <span data-ttu-id="faf80-219">Copia una stringa in un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-219">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="faf80-220">**StringCbCopyN**</span><span class="sxs-lookup"><span data-stu-id="faf80-220">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | <span data-ttu-id="faf80-221">Copia il numero specificato di byte da una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-221">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="faf80-222">**StringCbCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-222">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | <span data-ttu-id="faf80-223">Copia il numero specificato di byte da una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-223">Copies the specified number of bytes from one string to another.</span></span><br/>                      |
| [<span data-ttu-id="faf80-224">**StringCbGets**</span><span class="sxs-lookup"><span data-stu-id="faf80-224">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | <span data-ttu-id="faf80-225">Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="faf80-225">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="faf80-226">**StringCbGetsEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-226">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | <span data-ttu-id="faf80-227">Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="faf80-227">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="faf80-228">**StringCbLength**</span><span class="sxs-lookup"><span data-stu-id="faf80-228">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | <span data-ttu-id="faf80-229">Determina se una stringa supera la lunghezza specificata, in byte.</span><span class="sxs-lookup"><span data-stu-id="faf80-229">Determines whether a string exceeds the specified length, in bytes.</span></span><br/>                   |
| [<span data-ttu-id="faf80-230">**StringCbPrintf**</span><span class="sxs-lookup"><span data-stu-id="faf80-230">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | <span data-ttu-id="faf80-231">Scrive i dati formattati nella stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-231">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="faf80-232">**StringCbPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-232">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | <span data-ttu-id="faf80-233">Scrive i dati formattati nella stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-233">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="faf80-234">**StringCbVPrintf**</span><span class="sxs-lookup"><span data-stu-id="faf80-234">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | <span data-ttu-id="faf80-235">Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="faf80-235">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="faf80-236">**StringCbVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-236">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | <span data-ttu-id="faf80-237">Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="faf80-237">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="faf80-238">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="faf80-238">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | <span data-ttu-id="faf80-239">Concatena una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-239">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="faf80-240">**StringCchCatEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-240">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | <span data-ttu-id="faf80-241">Concatena una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-241">Concatenates one string to another string.</span></span><br/>                                            |
| [<span data-ttu-id="faf80-242">**StringCchCatN**</span><span class="sxs-lookup"><span data-stu-id="faf80-242">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | <span data-ttu-id="faf80-243">Concatena il numero specificato di caratteri da una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-243">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="faf80-244">**StringCchCatNEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-244">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | <span data-ttu-id="faf80-245">Concatena il numero specificato di caratteri da una stringa a un'altra stringa.</span><span class="sxs-lookup"><span data-stu-id="faf80-245">Concatenates the specified number of characters from one string to another string.</span></span><br/>    |
| [<span data-ttu-id="faf80-246">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="faf80-246">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | <span data-ttu-id="faf80-247">Copia una stringa in un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-247">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="faf80-248">**StringCchCopyEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-248">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | <span data-ttu-id="faf80-249">Copia una stringa in un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-249">Copies one string to another.</span></span><br/>                                                         |
| [<span data-ttu-id="faf80-250">**StringCchCopyN**</span><span class="sxs-lookup"><span data-stu-id="faf80-250">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | <span data-ttu-id="faf80-251">Copia il numero specificato di caratteri da una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-251">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="faf80-252">**StringCchCopyNEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-252">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | <span data-ttu-id="faf80-253">Copia il numero specificato di caratteri da una stringa a un'altra.</span><span class="sxs-lookup"><span data-stu-id="faf80-253">Copies the specified number of characters from one string to another.</span></span><br/>                 |
| [<span data-ttu-id="faf80-254">**StringCchGets**</span><span class="sxs-lookup"><span data-stu-id="faf80-254">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | <span data-ttu-id="faf80-255">Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="faf80-255">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="faf80-256">**StringCchGetsEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-256">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | <span data-ttu-id="faf80-257">Ottiene una riga di testo da stdin, fino a includere il carattere di nuova riga (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="faf80-257">Gets one line of text from stdin, up to and including the newline character ('\\n').</span></span><br/>  |
| [<span data-ttu-id="faf80-258">**StringCchLength**</span><span class="sxs-lookup"><span data-stu-id="faf80-258">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | <span data-ttu-id="faf80-259">Determina se una stringa supera la lunghezza specificata, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="faf80-259">Determines whether a string exceeds the specified length, in characters.</span></span><br/>              |
| [<span data-ttu-id="faf80-260">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="faf80-260">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | <span data-ttu-id="faf80-261">Scrive i dati formattati nella stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-261">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="faf80-262">**StringCchPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-262">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | <span data-ttu-id="faf80-263">Scrive i dati formattati nella stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="faf80-263">Writes formatted data to the specified string.</span></span><br/>                                        |
| [<span data-ttu-id="faf80-264">**StringCchVPrintf**</span><span class="sxs-lookup"><span data-stu-id="faf80-264">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | <span data-ttu-id="faf80-265">Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="faf80-265">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |
| [<span data-ttu-id="faf80-266">**StringCchVPrintfEx**</span><span class="sxs-lookup"><span data-stu-id="faf80-266">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | <span data-ttu-id="faf80-267">Scrive i dati formattati nella stringa specificata utilizzando un puntatore a un elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="faf80-267">Writes formatted data to the specified string using a pointer to a list of arguments.</span></span><br/> |



 

 

