---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRequired su una stringa che rappresenta il numero totale di byte necessari per tutte le funzionalità selezionate nel volume a cui fa riferimento la proprietà PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Proprietà PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333673"
---
# <a name="primaryvolumespacerequired-property"></a><span data-ttu-id="e26db-103">Proprietà PrimaryVolumeSpaceRequired</span><span class="sxs-lookup"><span data-stu-id="e26db-103">PrimaryVolumeSpaceRequired property</span></span>

<span data-ttu-id="e26db-104">Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceRequired** su una stringa che rappresenta il numero totale di byte necessari per tutte le funzionalità selezionate nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="e26db-104">The installer sets the value of the **PrimaryVolumeSpaceRequired** property to a string representing the total number of bytes required by all selected features on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span> <span data-ttu-id="e26db-105">Come per la proprietà [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , questo numero è espresso in unità di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="e26db-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e26db-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="e26db-106">Remarks</span></span>

<span data-ttu-id="e26db-107">Nota Se questo valore deve essere visualizzato in un [controllo testo](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare automaticamente ed etichettare questo numero in unità di kilobyte o megabyte, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="e26db-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e26db-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e26db-108">Requirements</span></span>



| <span data-ttu-id="e26db-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e26db-109">Requirement</span></span> | <span data-ttu-id="e26db-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e26db-110">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e26db-111">Versione</span><span class="sxs-lookup"><span data-stu-id="e26db-111">Version</span></span><br/> | <span data-ttu-id="e26db-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e26db-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e26db-113">Windows Installer 4,0 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e26db-113">Windows Installer 4.0 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e26db-114">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e26db-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e26db-115">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e26db-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e26db-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e26db-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e26db-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e26db-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




