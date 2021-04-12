---
description: Quando si usano stringhe con terminazione null, le applicazioni Unicode devono sempre eseguire il cast di zero a TCHAR.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Utilizzo di stringhe con terminazione null
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234191"
---
# <a name="using-null-terminated-strings"></a><span data-ttu-id="dd55a-103">Utilizzo di stringhe con terminazione null</span><span class="sxs-lookup"><span data-stu-id="dd55a-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="dd55a-104">Quando si usano stringhe con terminazione null, le applicazioni Unicode devono sempre eseguire il cast di zero a TCHAR.</span><span class="sxs-lookup"><span data-stu-id="dd55a-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="dd55a-105">Il codice 0x0000 è il carattere di terminazione della stringa Unicode per una stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="dd55a-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="dd55a-106">Un byte null singolo non è sufficiente per questo codice, perché molti caratteri Unicode contengono byte null come valore massimo o basso.</span><span class="sxs-lookup"><span data-stu-id="dd55a-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="dd55a-107">Un esempio è la lettera A, per cui il codice carattere è 0x0041.</span><span class="sxs-lookup"><span data-stu-id="dd55a-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd55a-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd55a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd55a-109">Utilizzo di caratteri speciali in Unicode</span><span class="sxs-lookup"><span data-stu-id="dd55a-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



