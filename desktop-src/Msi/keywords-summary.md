---
description: La proprietà riepilogo parole chiave nei database o nelle trasformazioni di installazione contiene un elenco di parole chiave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Proprietà di riepilogo parole chiave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330491"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="8c4e3-103">Proprietà di riepilogo parole chiave</span><span class="sxs-lookup"><span data-stu-id="8c4e3-103">Keywords Summary property</span></span>

<span data-ttu-id="8c4e3-104">La proprietà **Riepilogo parole chiave** nei database o nelle trasformazioni di installazione contiene un elenco di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="8c4e3-105">Le parole chiave possono essere usate dai browser di file per cercare un file.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="8c4e3-106">Questa proprietà contiene un elenco di origini della patch in un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="8c4e3-107">Per fornire il valore di questa proprietà nelle informazioni di riepilogo, spetta all'autore di un database di installazione, di una trasformazione o di un pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="8c4e3-108">Per determinare il valore corretto, gli autori devono eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="8c4e3-109">In un pacchetto di installazione, impostare il valore di questa proprietà su un elenco di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="8c4e3-110">La parola chiave deve includere "Installer", nonché parole chiave specifiche del prodotto, e può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="8c4e3-111">In una trasformazione, impostare il valore di questa proprietà su un elenco di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="8c4e3-112">La parola chiave deve includere "Installer", nonché parole chiave specifiche del prodotto, e può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="8c4e3-113">In un pacchetto di patch, impostare il valore di questa proprietà su un elenco delimitato da punti e virgola dei percorsi di rete o URL per le origini della patch.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="8c4e3-114">Quando la patch viene installata, il programma di installazione li aggiunge all'elenco di origine per il pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="8c4e3-115">Se la patch memorizzata nella cache risulta mancante, il programma di installazione può cercare un'origine nel percorso originale, un percorso aggiunto all'elenco di origine in base alla proprietà di **Riepilogo delle parole chiave** o un percorso aggiunto all'elenco di origine usando le funzioni [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) o [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .</span><span class="sxs-lookup"><span data-stu-id="8c4e3-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4e3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c4e3-116">Requirements</span></span>



| <span data-ttu-id="8c4e3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c4e3-117">Requirement</span></span> | <span data-ttu-id="8c4e3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8c4e3-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4e3-119">Versione</span><span class="sxs-lookup"><span data-stu-id="8c4e3-119">Version</span></span><br/> | <span data-ttu-id="8c4e3-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8c4e3-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c4e3-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8c4e3-122">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c4e3-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c4e3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c4e3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4e3-124">Descrizioni delle proprietà di riepilogo</span><span class="sxs-lookup"><span data-stu-id="8c4e3-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




