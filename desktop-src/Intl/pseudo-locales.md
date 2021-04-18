---
description: 'Windows Vista e versioni successive: NLS definisce diverse pseudo-impostazioni locali da utilizzare oltre alle impostazioni locali di Windows esistenti.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306604"
---
# <a name="pseudo-locales"></a><span data-ttu-id="de142-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="de142-103">Pseudo-Locales</span></span>

<span data-ttu-id="de142-104">**Windows Vista e versioni successive:** NLS definisce diverse pseudo-impostazioni locali da utilizzare oltre alle impostazioni locali di Windows esistenti.</span><span class="sxs-lookup"><span data-stu-id="de142-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="de142-105">Usare queste pseudo-impostazioni locali per testare la localizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="de142-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="de142-106">Per informazioni dettagliate sull'implementazione, vedere [uso di Pseudo-Locales per il test di localizzazione](using-pseudo-locales-for-localization-testing.md).</span><span class="sxs-lookup"><span data-stu-id="de142-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="de142-107">Pseudo-Locales supportati</span><span class="sxs-lookup"><span data-stu-id="de142-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="de142-108">Le pseudo-impostazioni locali supportate da NLS sono:</span><span class="sxs-lookup"><span data-stu-id="de142-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="de142-109">Pseudo-impostazioni locali di base</span><span class="sxs-lookup"><span data-stu-id="de142-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="de142-110">Pseudo-impostazioni locali con mirroring (da destra a sinistra)</span><span class="sxs-lookup"><span data-stu-id="de142-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="de142-111">Lingue asiatiche orientali-pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="de142-112">Scegliere le specifiche pseudo-impostazioni locali da usare in base alle assegnazioni della tabella codici e alle stringhe per la localizzazione, ad esempio i nomi dei mesi e dei giorni.</span><span class="sxs-lookup"><span data-stu-id="de142-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="de142-113">I dati per ogni pseudo-impostazioni locali includono non solo le tabelle codici pertinenti e le stringhe giorno e mese per la localizzazione, ma anche i dati per diversi altri test case per NLS.</span><span class="sxs-lookup"><span data-stu-id="de142-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="de142-114">I test case esaminano i tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="de142-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="de142-115">[identificatori delle impostazioni locali](locale-identifiers.md)a 9 bit.</span><span class="sxs-lookup"><span data-stu-id="de142-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="de142-116">Le pseudo-impostazioni locali offrono la possibilità di testare il funzionamento degli identificatori delle impostazioni locali a 9 bit.</span><span class="sxs-lookup"><span data-stu-id="de142-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="de142-117">Stringhe da linguaggi che devono usare tipi di carattere piccoli.</span><span class="sxs-lookup"><span data-stu-id="de142-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="de142-118">A causa delle limitazioni nell'interfaccia GDI (Graphics Device Interface), il tipo di carattere dell'interfaccia utente per alcune lingue è più piccolo di quello ottimale.</span><span class="sxs-lookup"><span data-stu-id="de142-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="de142-119">Le pseudo-impostazioni locali includono diverse stringhe di questi linguaggi, combinate con stringhe da linguaggi con una gestione dei tipi di carattere più standard.</span><span class="sxs-lookup"><span data-stu-id="de142-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="de142-120">È possibile utilizzare queste stringhe nei test per determinare come viene eseguito il rendering di un tipo di carattere limitato da GDI.</span><span class="sxs-lookup"><span data-stu-id="de142-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="de142-121">Lunghezze di stringa insolite.</span><span class="sxs-lookup"><span data-stu-id="de142-121">Unusual string lengths.</span></span> <span data-ttu-id="de142-122">Alcune costanti di informazioni sulle impostazioni locali, ad esempio [ \_ slist](locale-slist.md) delle impostazioni locali e [ \_ ICURRENCY delle impostazioni locali](locale-icurrency.md), presentano limiti convenzionali sulle dimensioni della stringa.</span><span class="sxs-lookup"><span data-stu-id="de142-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="de142-123">Le pseudo-impostazioni locali supportano l'esame delle diverse lunghezze di stringa.</span><span class="sxs-lookup"><span data-stu-id="de142-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="de142-124">Ordinamenti alternativi.</span><span class="sxs-lookup"><span data-stu-id="de142-124">Alternate sorts.</span></span> <span data-ttu-id="de142-125">Le pseudo-impostazioni locali possono essere usate per testare la funzionalità di ordinamento alternativo quando l' [identificatore](sort-order-identifiers.md) di ordinamento alternativo è diverso dall'identificatore di ordinamento di base che in genere è associato alle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="de142-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="de142-126">Identificatori e nomi di pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="de142-127">Le pseudo-impostazioni locali hanno [nomi di impostazioni locali](locale-names.md) scelti dallo spazio di utilizzo privato per evitare conflitti con le stringhe possibili introdotte negli standard organizzazione internazionale per la standardizzazione (iso) 639 e ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="de142-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="de142-128">Ogni pseudo-impostazioni locali dispone anche di un proprio identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="de142-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="de142-129">Nella tabella seguente sono riportati i nomi e gli identificatori per le pseudo-impostazioni locali definite.</span><span class="sxs-lookup"><span data-stu-id="de142-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="de142-130">Pseudo-impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-130">Pseudo-locale</span></span>       | <span data-ttu-id="de142-131">Nome delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-131">Locale name</span></span> | <span data-ttu-id="de142-132">Identificatore delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="de142-133">Base</span><span class="sxs-lookup"><span data-stu-id="de142-133">Base</span></span>                | <span data-ttu-id="de142-134">query al secondo-ploc</span><span class="sxs-lookup"><span data-stu-id="de142-134">qps-ploc</span></span>    | <span data-ttu-id="de142-135">0501</span><span class="sxs-lookup"><span data-stu-id="de142-135">0501</span></span>              |
| <span data-ttu-id="de142-136">Con mirroring</span><span class="sxs-lookup"><span data-stu-id="de142-136">Mirrored</span></span>            | <span data-ttu-id="de142-137">query al secondo-plocm</span><span class="sxs-lookup"><span data-stu-id="de142-137">qps-plocm</span></span>   | <span data-ttu-id="de142-138">09ff</span><span class="sxs-lookup"><span data-stu-id="de142-138">09ff</span></span>              |
| <span data-ttu-id="de142-139">Asia orientale-lingua</span><span class="sxs-lookup"><span data-stu-id="de142-139">East Asian-language</span></span> | <span data-ttu-id="de142-140">query al secondo-Besca</span><span class="sxs-lookup"><span data-stu-id="de142-140">qps-ploca</span></span>   | <span data-ttu-id="de142-141">05fe</span><span class="sxs-lookup"><span data-stu-id="de142-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="de142-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="de142-142">Example</span></span>

<span data-ttu-id="de142-143">Nell'esempio seguente viene illustrato il testo visualizzato per le pseudo-impostazioni locali di base:</span><span class="sxs-lookup"><span data-stu-id="de142-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="de142-144">\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ!! \] ōf 2006</span><span class="sxs-lookup"><span data-stu-id="de142-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="de142-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de142-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de142-146">Impostazioni locali e lingue</span><span class="sxs-lookup"><span data-stu-id="de142-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="de142-147">Identificatori delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="de142-148">Nomi delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="de142-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="de142-149">Identificatori di ordinamento</span><span class="sxs-lookup"><span data-stu-id="de142-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="de142-150">Uso di Pseudo-Locales per il test di localizzazione</span><span class="sxs-lookup"><span data-stu-id="de142-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



