---
description: L'impostazione della proprietà SHORTFILENAMES causa l'utilizzo di nomi di file brevi per i nomi dei file di destinazione, anziché nomi di file lunghi. Non influisce sui nomi di file che il programma di installazione cerca nell'origine.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Proprietà SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333669"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="f422f-104">Proprietà SHORTFILENAMES</span><span class="sxs-lookup"><span data-stu-id="f422f-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="f422f-105">L'impostazione della proprietà **SHORTFILENAMES** causa l'utilizzo di nomi di file brevi per i nomi dei file di destinazione, anziché nomi di file lunghi.</span><span class="sxs-lookup"><span data-stu-id="f422f-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="f422f-106">Non influisce sui nomi di file che il programma di installazione cerca nell'origine.</span><span class="sxs-lookup"><span data-stu-id="f422f-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="f422f-107">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="f422f-107">Default Value</span></span>

<span data-ttu-id="f422f-108">I nomi lunghi vengono usati dal programma di installazione se la proprietà **SHORTFILENAMES** non è impostata e il volume di destinazione supporta nomi lunghi.</span><span class="sxs-lookup"><span data-stu-id="f422f-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="f422f-109">I nomi brevi vengono usati dal programma di installazione se il volume di destinazione non supporta nomi lunghi.</span><span class="sxs-lookup"><span data-stu-id="f422f-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="f422f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f422f-110">Remarks</span></span>

<span data-ttu-id="f422f-111">Quando viene impostata la proprietà **SHORTFILENAMES** , il programma di installazione crea le cartelle e installa i file usando nomi di file brevi da qualsiasi coppia di brevi \| lunghezza elencata nella [tabella file](file-table.md) o nella [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f422f-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="f422f-112">Le applicazioni possono utilizzare la funzione [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) per recuperare il formato di percorso breve di un percorso di file specificato.</span><span class="sxs-lookup"><span data-stu-id="f422f-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="f422f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f422f-113">Requirements</span></span>



| <span data-ttu-id="f422f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f422f-114">Requirement</span></span> | <span data-ttu-id="f422f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f422f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f422f-116">Versione</span><span class="sxs-lookup"><span data-stu-id="f422f-116">Version</span></span><br/> | <span data-ttu-id="f422f-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f422f-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f422f-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f422f-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f422f-119">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f422f-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f422f-120">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f422f-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f422f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f422f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f422f-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f422f-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 
