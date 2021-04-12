---
description: Costanti di \_ restituzione delle impostazioni locali \*
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Costanti LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233308"
---
# <a name="locale_return-constants"></a><span data-ttu-id="bd305-103">Costanti di \_ restituzione delle impostazioni locali \*</span><span class="sxs-lookup"><span data-stu-id="bd305-103">LOCALE\_RETURN\* Constants</span></span>

<span data-ttu-id="bd305-104">Questo argomento definisce le \_ costanti di restituzione delle impostazioni locali \* usate da NLS.</span><span class="sxs-lookup"><span data-stu-id="bd305-104">This topic defines the LOCALE\_RETURN\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd305-105">Valore</span><span class="sxs-lookup"><span data-stu-id="bd305-105">Value</span></span></th>
<th><span data-ttu-id="bd305-106">Significato</span><span class="sxs-lookup"><span data-stu-id="bd305-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd305-107">LOCALE_RETURN_GENITIVE_NAMES</span><span class="sxs-lookup"><span data-stu-id="bd305-107">LOCALE_RETURN_GENITIVE_NAMES</span></span></td>
<td><span data-ttu-id="bd305-108"><strong>Windows 7 e versioni successive:</strong> Recuperare i nomi di genitive dei mesi, ovvero i nomi usati quando i nomi dei mesi vengono combinati con altri elementi.</span><span class="sxs-lookup"><span data-stu-id="bd305-108"><strong>Windows 7 and later:</strong> Retrieve the genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="bd305-109">Ad esempio, in ucraino l'equivalente di gennaio viene scritto &quot; Січень &quot; quando il mese è denominato da solo.</span><span class="sxs-lookup"><span data-stu-id="bd305-109">For example, in Ukrainian the equivalent of January is written &quot;Січень&quot; when the month is named alone.</span></span> <span data-ttu-id="bd305-110">Tuttavia, quando il nome del mese viene usato in combinazione, ad esempio, in una data, ad esempio il 5 gennaio 2003, viene usata la forma genitiva del nome.</span><span class="sxs-lookup"><span data-stu-id="bd305-110">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="bd305-111">Per l'esempio ucraino, il nome del mese del genico viene visualizzato come &quot; 5 січня 2003 &quot; .</span><span class="sxs-lookup"><span data-stu-id="bd305-111">For the Ukrainian example, the genitive month name is displayed as &quot;5 січня 2003&quot;.</span></span> <span data-ttu-id="bd305-112">L'elenco dei nomi dei mesi di genitive inizia con gennaio e è delimitato da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="bd305-112">The list of genitive month names begins with January and is semicolon-delimited.</span></span> <span data-ttu-id="bd305-113">Se non è presente alcun tredicesimo mese, utilizzare un punto e virgola al suo posto alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="bd305-113">If there is no 13th month, use a semicolon in its place at the end of the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="bd305-114">I nomi dei mesi di genitive non esistono in tutte le lingue.</span><span class="sxs-lookup"><span data-stu-id="bd305-114">Genitive month names do not exist in all languages.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd305-115">LOCALE_RETURN_NUMBER</span><span class="sxs-lookup"><span data-stu-id="bd305-115">LOCALE_RETURN_NUMBER</span></span></td>
<td><span data-ttu-id="bd305-116"><strong>Windows Me/98, Windows NT 4,0 e versioni successive:</strong> Recuperare un numero.</span><span class="sxs-lookup"><span data-stu-id="bd305-116"><strong>Windows Me/98, Windows NT 4.0 and later:</strong> Retrieve a number.</span></span> <span data-ttu-id="bd305-117">Questa costante fa in modo che <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperi un valore come numero anziché come stringa.</span><span class="sxs-lookup"><span data-stu-id="bd305-117">This constant causes <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> to retrieve a value as a number instead of as a string.</span></span> <span data-ttu-id="bd305-118">Il buffer che riceve il valore deve essere almeno la lunghezza di un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="bd305-118">The buffer that receives the value must be at least the length of a DWORD value.</span></span> <span data-ttu-id="bd305-119">Questa costante può essere combinata con qualsiasi altra costante con un nome che inizia con &quot; LOCALE_I &quot; .</span><span class="sxs-lookup"><span data-stu-id="bd305-119">This constant can be combined with any other constant having a name that begins with &quot;LOCALE_I&quot;.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




