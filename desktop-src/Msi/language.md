---
description: Il tipo di dati Language è una stringa di testo contenente uno o più ID di lingua numerici validi. Se sono presenti due o più ID lingua, devono essere separati da virgole.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Linguaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226124"
---
# <a name="language"></a><span data-ttu-id="6231b-104">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="6231b-104">Language</span></span>

<span data-ttu-id="6231b-105">Il tipo di dati Language è una stringa di testo contenente uno o più ID di lingua numerici validi.</span><span class="sxs-lookup"><span data-stu-id="6231b-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="6231b-106">Se sono presenti due o più ID lingua, devono essere separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="6231b-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="6231b-107">Il tipo di dati Language è un valore a 16 bit costituito dalla combinazione di ID numerici primari e sottolinguaggi.</span><span class="sxs-lookup"><span data-stu-id="6231b-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="6231b-108">Il LANGID primario include i bit da 0 a 9 mentre l'ID del sottolingua è BITS da 10 a 15.</span><span class="sxs-lookup"><span data-stu-id="6231b-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="6231b-109">Per un elenco degli identificatori numerici primari e secondari, vedere l'argomento relativo alle [costanti e alle stringhe dell'identificatore di lingua](../intl/language-identifier-constants-and-strings.md) .</span><span class="sxs-lookup"><span data-stu-id="6231b-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="6231b-110">Per gli ID della lingua primaria, l'intervallo da 0x200 a 0x3FF è definibile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6231b-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="6231b-111">L'intervallo da 0x000 a 0x1FF è riservato per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="6231b-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="6231b-112">Per gli ID del linguaggio secondario, l'intervallo da 0x20 a 0x3F è definibile dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6231b-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="6231b-113">L'intervallo da 0x00 a 0x1F è riservato per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="6231b-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
