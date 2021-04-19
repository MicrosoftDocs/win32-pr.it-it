---
description: La proprietà ROOTDRIVE Specifica l'unità predefinita per la directory di destinazione dell'installazione.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: Proprietà ROOTDRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326369"
---
# <a name="rootdrive-property"></a><span data-ttu-id="aa09b-103">Proprietà ROOTDRIVE</span><span class="sxs-lookup"><span data-stu-id="aa09b-103">ROOTDRIVE property</span></span>

<span data-ttu-id="aa09b-104">La proprietà **ROOTDRIVE** specifica l'unità predefinita per la directory di destinazione dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="aa09b-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="aa09b-105">Se nella colonna directory della [tabella directory](directory-table.md) è indicata la directory di destinazione radice in base a un nome di proprietà non definito, il programma di installazione utilizzerà il valore della proprietà **ROOTDRIVE** per risolvere il percorso della directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="aa09b-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="aa09b-106">Se **ROOTDRIVE** non è impostato a una riga di comando o creato nella [tabella delle proprietà](property-table.md), il programma di installazione imposta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="aa09b-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="aa09b-107">Durante un' [installazione amministrativa](administrative-installation.md) , il programma di installazione imposta **ROOTDRIVE** sulla prima unità di rete connessa che trova in cui è possibile scrivere.</span><span class="sxs-lookup"><span data-stu-id="aa09b-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="aa09b-108">Se non si tratta di un'installazione amministrativa o se il programma di installazione non è in grado di trovare unità di rete, il programma di installazione imposta **ROOTDRIVE** sull'unità locale che può essere scritta per avere maggiore spazio libero.</span><span class="sxs-lookup"><span data-stu-id="aa09b-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="aa09b-109">Il valore di questa proprietà deve terminare con ' \\ '.</span><span class="sxs-lookup"><span data-stu-id="aa09b-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa09b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa09b-110">Requirements</span></span>



| <span data-ttu-id="aa09b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa09b-111">Requirement</span></span> | <span data-ttu-id="aa09b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="aa09b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa09b-113">Versione</span><span class="sxs-lookup"><span data-stu-id="aa09b-113">Version</span></span><br/> | <span data-ttu-id="aa09b-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa09b-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aa09b-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aa09b-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aa09b-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aa09b-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="aa09b-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="aa09b-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa09b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa09b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa09b-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aa09b-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




