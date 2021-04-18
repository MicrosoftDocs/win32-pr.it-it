---
description: La proprietà SOURCE list è un elenco delimitato da punti e virgola di percorsi di origine di rete o URL per il pacchetto di installazione dell'applicazione.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCEs (proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324852"
---
# <a name="sourcelist-property"></a><span data-ttu-id="9a0c3-103">SOURCEs (proprietà)</span><span class="sxs-lookup"><span data-stu-id="9a0c3-103">SOURCELIST property</span></span>

<span data-ttu-id="9a0c3-104">La proprietà **source** list è un elenco delimitato da punti e virgola di percorsi di origine di rete o URL per il pacchetto di installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="9a0c3-105">Questo elenco viene aggiunto alla fine dell'elenco di origine di ogni utente esistente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="9a0c3-106">Il programma di installazione individua un'origine enumerando l'elenco dei percorsi di origine e usa il primo percorso accessibile individuato.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="9a0c3-107">Solo questa origine può essere utilizzata per il resto dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="9a0c3-108">Ogni percorso specificato nell'elenco di origine deve quindi essere un percorso che disponga di un'origine completa per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="9a0c3-109">L'intero albero di directory in ogni percorso di origine deve essere lo stesso e deve includere tutti i file di origine necessari, inclusi tutti i file CAB.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="9a0c3-110">Ogni percorso deve avere un file con estensione msi con lo stesso nome file e il codice prodotto.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="9a0c3-111">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="9a0c3-111">Default Value</span></span>

<span data-ttu-id="9a0c3-112">Il programma di installazione controlla solo la proprietà **SourceName** se il prodotto non è già stato pubblicizzato o installato.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="9a0c3-113">In tutti gli altri casi, il programma di installazione usa l'elenco di origine esistente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0c3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a0c3-114">Remarks</span></span>

<span data-ttu-id="9a0c3-115">Le origini aggiunte utilizzando la proprietà di **origine** vengono aggiunte direttamente alla fine dell'elenco per ogni tipo di origine e si trovano sempre dopo l'origine predefinita specificata dalla proprietà [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="9a0c3-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="9a0c3-116">Per Windows Installer il numero di origini nella proprietà di **origine** è illimitato.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="9a0c3-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) può essere usato per aggiungere origini di rete.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0c3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a0c3-118">Requirements</span></span>



| <span data-ttu-id="9a0c3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a0c3-119">Requirement</span></span> | <span data-ttu-id="9a0c3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9a0c3-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0c3-121">Versione</span><span class="sxs-lookup"><span data-stu-id="9a0c3-121">Version</span></span><br/> | <span data-ttu-id="9a0c3-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9a0c3-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9a0c3-124">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9a0c3-125">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9a0c3-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9a0c3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a0c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0c3-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9a0c3-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9a0c3-128">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="9a0c3-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




