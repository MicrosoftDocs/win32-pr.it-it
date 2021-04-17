---
description: Le applicazioni devono usare il carattere separatore di riga (0x2028) e il carattere separatore di paragrafo (0x2029) per dividere il testo normale. Viene iniziata una nuova riga dopo ogni separatore di riga. Viene iniziato un nuovo paragrafo dopo ogni separatore di paragrafo.
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: Uso dei separatori di riga e paragrafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9511ba2a8889b3c9139daf1d088d91ed746db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234194"
---
# <a name="using-line-and-paragraph-separators"></a><span data-ttu-id="98f0a-105">Uso dei separatori di riga e paragrafo</span><span class="sxs-lookup"><span data-stu-id="98f0a-105">Using Line and Paragraph Separators</span></span>

<span data-ttu-id="98f0a-106">Le applicazioni devono usare il carattere separatore di riga (0x2028) e il carattere separatore di paragrafo (0x2029) per dividere il testo normale.</span><span class="sxs-lookup"><span data-stu-id="98f0a-106">Your applications should use the line separator character (0x2028) and the paragraph separator character (0x2029) to divide plain text.</span></span> <span data-ttu-id="98f0a-107">Viene iniziata una nuova riga dopo ogni separatore di riga.</span><span class="sxs-lookup"><span data-stu-id="98f0a-107">A new line is begun after each line separator.</span></span> <span data-ttu-id="98f0a-108">Viene iniziato un nuovo paragrafo dopo ogni separatore di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="98f0a-108">A new paragraph is begun after each paragraph separator.</span></span>

<span data-ttu-id="98f0a-109">Non è necessario avviare la prima riga o paragrafo di un file con questi caratteri oppure per terminare l'ultima riga o paragrafo.</span><span class="sxs-lookup"><span data-stu-id="98f0a-109">It is not necessary to start the first line or paragraph in a file with these characters, or to end the last line or paragraph with them.</span></span> <span data-ttu-id="98f0a-110">Questa operazione indica che è presente una riga o un paragrafo vuoto in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="98f0a-110">Doing so indicates that there is an empty line or paragraph in that location.</span></span>

<span data-ttu-id="98f0a-111">L'applicazione può usare il separatore di riga per indicare una fine della riga non condizionale.</span><span class="sxs-lookup"><span data-stu-id="98f0a-111">The application can use the line separator to indicate an unconditional end of line.</span></span> <span data-ttu-id="98f0a-112">I separatori di riga, tuttavia, non corrispondono a una sequenza separata di caratteri di ritorno a capo e avanzamento di riga o a una combinazione di questi caratteri.</span><span class="sxs-lookup"><span data-stu-id="98f0a-112">However, line separators do not correspond to the separate carriage return and linefeed characters, or to a combination of these characters.</span></span> <span data-ttu-id="98f0a-113">I separatori di riga devono essere elaborati separatamente dai caratteri di ritorno a capo e avanzamento di riga.</span><span class="sxs-lookup"><span data-stu-id="98f0a-113">Line separators must be processed separately from carriage return and linefeed characters.</span></span>

<span data-ttu-id="98f0a-114">L'applicazione può inserire un separatore di paragrafo tra i paragrafi di testo.</span><span class="sxs-lookup"><span data-stu-id="98f0a-114">The application can insert a paragraph separator between paragraphs of text.</span></span> <span data-ttu-id="98f0a-115">L'uso di questo separatore consente la creazione di file di testo normale che possono essere formattati con larghezze di riga diverse su sistemi operativi diversi.</span><span class="sxs-lookup"><span data-stu-id="98f0a-115">Use of this separator allows creation of plain text files that can be formatted with different line widths on different operating systems.</span></span> <span data-ttu-id="98f0a-116">Il sistema di destinazione può ignorare eventuali separatori di riga e interrompere i paragrafi solo in corrispondenza di separatori di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="98f0a-116">The target system can ignore any line separators and break paragraphs only at the paragraph separators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98f0a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98f0a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98f0a-118">Utilizzo di caratteri speciali in Unicode</span><span class="sxs-lookup"><span data-stu-id="98f0a-118">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



