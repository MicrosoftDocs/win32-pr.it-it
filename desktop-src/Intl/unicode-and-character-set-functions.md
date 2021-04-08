---
description: Le funzioni seguenti vengono utilizzate con i set di caratteri.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funzioni del set di caratteri e Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058075"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="778e6-103">Funzioni del set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="778e6-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="778e6-104">Le funzioni seguenti vengono utilizzate con i set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="778e6-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="778e6-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="778e6-105">Function</span></span>                                                       | <span data-ttu-id="778e6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="778e6-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="778e6-107">**GetTextCharset**</span><span class="sxs-lookup"><span data-stu-id="778e6-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="778e6-108">Recupera un identificatore del set di caratteri per il tipo di carattere attualmente selezionato in un contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="778e6-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="778e6-109">**GetTextCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="778e6-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="778e6-110">Recupera le informazioni sul set di caratteri del tipo di carattere attualmente selezionato in un contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="778e6-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="778e6-111">**IsDBCSLeadByte**</span><span class="sxs-lookup"><span data-stu-id="778e6-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="778e6-112">Determina se un carattere specificato è un byte di apertura per la tabella codici ANSI di Windows predefinita del sistema (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="778e6-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="778e6-113">**IsDBCSLeadByteEx**</span><span class="sxs-lookup"><span data-stu-id="778e6-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="778e6-114">Determina se un carattere specificato è potenzialmente un byte di apertura.</span><span class="sxs-lookup"><span data-stu-id="778e6-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="778e6-115">**IsTextUnicode**</span><span class="sxs-lookup"><span data-stu-id="778e6-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="778e6-116">Determina se un buffer può contenere un formato di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="778e6-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="778e6-117">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="778e6-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="778e6-118">Esegue il mapping di una stringa di caratteri a una stringa UTF-16 (carattere wide).</span><span class="sxs-lookup"><span data-stu-id="778e6-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="778e6-119">**TranslateCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="778e6-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="778e6-120">Converte le informazioni sul set di caratteri e imposta tutti i membri di una struttura di destinazione sui valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="778e6-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="778e6-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="778e6-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="778e6-122">Esegue il mapping di una stringa UTF-16 (carattere wide) a una nuova stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="778e6-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="778e6-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="778e6-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="778e6-124">Non usare.</span><span class="sxs-lookup"><span data-stu-id="778e6-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="778e6-125">**NlsDllCodePageTranslation**</span><span class="sxs-lookup"><span data-stu-id="778e6-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="778e6-126">Non usare.</span><span class="sxs-lookup"><span data-stu-id="778e6-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="778e6-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="778e6-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="778e6-128">Non usare.</span><span class="sxs-lookup"><span data-stu-id="778e6-128">Do not use.</span></span>                                                                                                           |



 

 

 
