---
description: Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRemaining su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà PrimaryVolumePath, se tutte le funzionalità attualmente selezionate sono state installate.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Proprietà PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333672"
---
# <a name="primaryvolumespaceremaining-property"></a><span data-ttu-id="ac082-103">Proprietà PrimaryVolumeSpaceRemaining</span><span class="sxs-lookup"><span data-stu-id="ac082-103">PrimaryVolumeSpaceRemaining property</span></span>

<span data-ttu-id="ac082-104">Il programma di installazione imposta il valore della proprietà **PrimaryVolumeSpaceRemaining** su una stringa che rappresenta il numero totale di byte rimanenti nel volume a cui fa riferimento la proprietà [**PrimaryVolumePath**](primaryvolumepath.md) , se tutte le funzionalità attualmente selezionate sono state installate.</span><span class="sxs-lookup"><span data-stu-id="ac082-104">The installer sets the value of the **PrimaryVolumeSpaceRemaining** property to a string representing the total number of bytes remaining on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property, if all currently selected features were installed.</span></span> <span data-ttu-id="ac082-105">Come per la proprietà [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , questo numero è espresso in unità di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="ac082-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac082-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac082-106">Remarks</span></span>

<span data-ttu-id="ac082-107">Nota Se questo valore deve essere visualizzato in un [controllo testo](text-control.md)statico, il bit [FormatSize](formatsize-control-attribute.md) può essere usato per formattare automaticamente ed etichettare questo numero in unità di kilobyte o megabyte, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="ac082-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac082-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac082-108">Requirements</span></span>



| <span data-ttu-id="ac082-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac082-109">Requirement</span></span> | <span data-ttu-id="ac082-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ac082-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac082-111">Versione</span><span class="sxs-lookup"><span data-stu-id="ac082-111">Version</span></span><br/> | <span data-ttu-id="ac082-112">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ac082-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ac082-113">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ac082-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ac082-114">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="ac082-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac082-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac082-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac082-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac082-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




