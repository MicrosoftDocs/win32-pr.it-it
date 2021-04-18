---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceAvailable su una stringa che rappresenta il numero totale di byte disponibili, in unità di 512, nel volume a cui fa riferimento la proprietà PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Proprietà PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327801"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="4453a-103">Proprietà PrimaryVolumeSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="4453a-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="4453a-104">Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceAvailable** su una stringa che rappresenta il numero totale di byte disponibili, in unità di 512, nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="4453a-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="4453a-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="4453a-105">Remarks</span></span>

<span data-ttu-id="4453a-106">Ad esempio, se [**PrimaryVolumePath**](primaryvolumepath.md) è impostato su "D:" e volume D: include 446.134.272 byte disponibili, **PrimaryVolumeSpaceAvailable** viene impostato su 871356.</span><span class="sxs-lookup"><span data-stu-id="4453a-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="4453a-107">Nota Se questo valore deve essere visualizzato in un [controllo testo](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare automaticamente ed etichettare questo numero in unità di kilobyte o megabyte, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="4453a-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4453a-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4453a-108">Requirements</span></span>



| <span data-ttu-id="4453a-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="4453a-109">Requirement</span></span> | <span data-ttu-id="4453a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="4453a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4453a-111">Versione</span><span class="sxs-lookup"><span data-stu-id="4453a-111">Version</span></span><br/> | <span data-ttu-id="4453a-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4453a-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4453a-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4453a-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4453a-114">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4453a-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4453a-115">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4453a-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4453a-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4453a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4453a-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4453a-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




