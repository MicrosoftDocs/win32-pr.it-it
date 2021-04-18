---
description: Le funzioni elencate nella tabella seguente consentono di convertire le stringhe di caratteri da un tipo stringa a un altro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversione tra tipi di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312852"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="4160c-103">Conversione tra tipi di stringa</span><span class="sxs-lookup"><span data-stu-id="4160c-103">Translation Between String Types</span></span>

<span data-ttu-id="4160c-104">Le funzioni elencate nella tabella seguente consentono di convertire le stringhe di caratteri da un tipo stringa a un altro.</span><span class="sxs-lookup"><span data-stu-id="4160c-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="4160c-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="4160c-105">Function</span></span>                                           | <span data-ttu-id="4160c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4160c-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="4160c-107">**Della funzione FoldString**</span><span class="sxs-lookup"><span data-stu-id="4160c-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="4160c-108">Converte una stringa di caratteri in un'altra.</span><span class="sxs-lookup"><span data-stu-id="4160c-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="4160c-109">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="4160c-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="4160c-110">Esegue il mapping di una stringa di caratteri in base alle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="4160c-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="4160c-111">**Tounicode**</span><span class="sxs-lookup"><span data-stu-id="4160c-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="4160c-112">Converte un codice di chiave virtuale in un carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="4160c-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="4160c-113">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="4160c-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="4160c-114">Esegue il mapping di una stringa multibyte a una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="4160c-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="4160c-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="4160c-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="4160c-116">Esegue il mapping di una stringa Unicode a una stringa multibyte.</span><span class="sxs-lookup"><span data-stu-id="4160c-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="4160c-117">Le funzioni [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sono particolarmente utili per le applicazioni che supportano più tipi di stringa.</span><span class="sxs-lookup"><span data-stu-id="4160c-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="4160c-118">ANSI C definisce anche le funzioni di conversione **wcstombs** e **mbstowcs**, ma possono solo eseguire la conversione da e verso il set di caratteri supportato dalla libreria C standard.</span><span class="sxs-lookup"><span data-stu-id="4160c-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4160c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4160c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4160c-120">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="4160c-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
