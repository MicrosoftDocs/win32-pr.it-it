---
description: È possibile utilizzare la proprietà MsiHiddenProperties per impedire al programma di installazione di visualizzare le password o altre informazioni riservate nel file di log.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Proprietà MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329249"
---
# <a name="msihiddenproperties-property"></a><span data-ttu-id="77e79-103">Proprietà MsiHiddenProperties</span><span class="sxs-lookup"><span data-stu-id="77e79-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="77e79-104">È possibile utilizzare la proprietà **MsiHiddenProperties** per impedire al programma di installazione di visualizzare le password o altre informazioni riservate nel file di log.</span><span class="sxs-lookup"><span data-stu-id="77e79-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="77e79-105">Per impedire che una proprietà venga scritta nel file di log, impostare il valore della proprietà **MsiHiddenProperties** sul nome della proprietà che si desidera nascondere.</span><span class="sxs-lookup"><span data-stu-id="77e79-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="77e79-106">È possibile nascondere più proprietà specificando una stringa di nomi di proprietà delimitati da punti e virgola (;).</span><span class="sxs-lookup"><span data-stu-id="77e79-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="77e79-107">Quando il criterio di [debug](debug.md) è impostato su un valore pari a 7, il programma di installazione scriverà le informazioni immesse in una riga di comando nel log.</span><span class="sxs-lookup"><span data-stu-id="77e79-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="77e79-108">In questo modo le proprietà pubbliche immesse in una riga di comando risultano visibili anche se la proprietà è inclusa nella proprietà **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="77e79-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="77e79-109">In questo modo, le informazioni riservate possono essere inserite in una riga di comando visibile nel log.</span><span class="sxs-lookup"><span data-stu-id="77e79-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="77e79-110">Per ulteriori informazioni, vedere [impedire che le informazioni riservate vengano scritte nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="77e79-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="77e79-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77e79-111">Requirements</span></span>



| <span data-ttu-id="77e79-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e79-112">Requirement</span></span> | <span data-ttu-id="77e79-113">Valore</span><span class="sxs-lookup"><span data-stu-id="77e79-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e79-114">Versione</span><span class="sxs-lookup"><span data-stu-id="77e79-114">Version</span></span><br/> | <span data-ttu-id="77e79-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="77e79-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="77e79-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="77e79-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="77e79-117">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77e79-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="77e79-118">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="77e79-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77e79-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77e79-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e79-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="77e79-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




