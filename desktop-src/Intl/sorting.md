---
description: Per NLS, ordinamento (noto anche come &\# 0034; collation&\# 0034;) è la disposizione delle stringhe.
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: Ordinamento (internazionalizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f49a5abb8371a00ad9ee63f929b4aaf4b18b11be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234049"
---
# <a name="sorting"></a><span data-ttu-id="9ddfd-103">Ordinamento</span><span class="sxs-lookup"><span data-stu-id="9ddfd-103">Sorting</span></span>

<span data-ttu-id="9ddfd-104">Per NLS, l'ordinamento (noto anche come "regole di confronto") è la disposizione delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-104">For NLS, sorting (also known as "collation") is the arrangement of strings.</span></span> <span data-ttu-id="9ddfd-105">Esistono due tipi di ordinamento:</span><span class="sxs-lookup"><span data-stu-id="9ddfd-105">There are two types of sorting:</span></span>

-   <span data-ttu-id="9ddfd-106">Ordinamento linguistico.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-106">Linguistic sorting.</span></span> <span data-ttu-id="9ddfd-107">Dispone le stringhe con caratteristiche linguistiche simili in gruppi (per ordinamento).</span><span class="sxs-lookup"><span data-stu-id="9ddfd-107">Arranges strings with similar linguistic characteristics into groups (by sorts).</span></span>
-   <span data-ttu-id="9ddfd-108">Ordinamento ordinale (non linguistico).</span><span class="sxs-lookup"><span data-stu-id="9ddfd-108">Ordinal (non-linguistic) sorting.</span></span> <span data-ttu-id="9ddfd-109">Dispone le stringhe in una sequenza ordinata.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-109">Arranges the strings in an ordered sequence.</span></span>

<span data-ttu-id="9ddfd-110">L'ordinamento usa le funzioni di confronto delle stringhe NLS, ad esempio [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), o le funzioni API "wrapper", ad esempio [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), che chiamano internamente le funzioni di confronto delle stringhe NLS.</span><span class="sxs-lookup"><span data-stu-id="9ddfd-110">Sorting uses the NLS string comparison functions, such as [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) and [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), or "wrapper" API functions, such as [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), that internally call the NLS string comparison functions.</span></span>

<span data-ttu-id="9ddfd-111">Per informazioni dettagliate sull'implementazione dell'ordinamento nelle applicazioni, vedere [gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).</span><span class="sxs-lookup"><span data-stu-id="9ddfd-111">For details about implementing sorting in your applications, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ddfd-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ddfd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ddfd-113">Informazioni sul supporto linguistico nazionale</span><span class="sxs-lookup"><span data-stu-id="9ddfd-113">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="9ddfd-114">Gestione dell'ordinamento nelle applicazioni</span><span class="sxs-lookup"><span data-stu-id="9ddfd-114">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> <dt>

[<span data-ttu-id="9ddfd-115">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="9ddfd-115">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[<span data-ttu-id="9ddfd-116">LCMapString</span><span class="sxs-lookup"><span data-stu-id="9ddfd-116">LCMapString</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
