---
description: L'impostazione di questo criterio di sistema per utente specifica l'ordine in cui il programma di installazione esegue la ricerca di tre tipi di origini.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885690"
---
# <a name="searchorder"></a><span data-ttu-id="e37dd-103">SearchOrder</span><span class="sxs-lookup"><span data-stu-id="e37dd-103">SearchOrder</span></span>

<span data-ttu-id="e37dd-104">L'impostazione di questo [criterio di sistema](system-policy.md) per utente specifica l'ordine in cui il programma di installazione esegue la ricerca di tre tipi di origini.</span><span class="sxs-lookup"><span data-stu-id="e37dd-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="e37dd-105">I tipi di origini sono:</span><span class="sxs-lookup"><span data-stu-id="e37dd-105">The types of sources are:</span></span>

<span data-ttu-id="e37dd-106">"n"-rete</span><span class="sxs-lookup"><span data-stu-id="e37dd-106">"n" – network</span></span>

<span data-ttu-id="e37dd-107">"m"-supporto (CD-ROM o DVD)</span><span class="sxs-lookup"><span data-stu-id="e37dd-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="e37dd-108">"u"-Uniform Resource Locator (URL)</span><span class="sxs-lookup"><span data-stu-id="e37dd-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="e37dd-109">Ad esempio, per cercare prima origini di rete, origini multimediali secondo e origini URL, impostare questo criterio su un valore "NMU".</span><span class="sxs-lookup"><span data-stu-id="e37dd-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="e37dd-110">Per omettere la ricerca di un particolare tipo di origine, lasciare la lettera corrispondente dal valore.</span><span class="sxs-lookup"><span data-stu-id="e37dd-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="e37dd-111">Se SearchOrder non è impostato, l'ordine di ricerca predefinito è rete, supporto e URL.</span><span class="sxs-lookup"><span data-stu-id="e37dd-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="e37dd-112">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e37dd-112">Registry Key</span></span>

<span data-ttu-id="e37dd-113">**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="e37dd-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e37dd-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e37dd-114">Data Type</span></span>

<span data-ttu-id="e37dd-115">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e37dd-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e37dd-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e37dd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e37dd-117">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="e37dd-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



