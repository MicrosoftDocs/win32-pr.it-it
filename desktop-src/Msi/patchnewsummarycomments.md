---
description: La proprietà PATCHNEWSUMMARYCOMMENTS aggiorna la proprietà di riepilogo dei commenti di un'installazione amministrativa durante l'applicazione di patch.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Proprietà PATCHNEWSUMMARYCOMMENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325719"
---
# <a name="patchnewsummarycomments-property"></a><span data-ttu-id="a114a-103">Proprietà PATCHNEWSUMMARYCOMMENTS</span><span class="sxs-lookup"><span data-stu-id="a114a-103">PATCHNEWSUMMARYCOMMENTS property</span></span>

<span data-ttu-id="a114a-104">La proprietà **PATCHNEWSUMMARYCOMMENTS** aggiorna la proprietà di [**Riepilogo dei commenti**](comments-summary.md) di un'installazione amministrativa durante l'applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="a114a-104">The **PATCHNEWSUMMARYCOMMENTS** property updates the [**Comments Summary**](comments-summary.md) property of an administrative installation during patching.</span></span> <span data-ttu-id="a114a-105">Questa proprietà viene impostata solo da una trasformazione in un file con estensione msp.</span><span class="sxs-lookup"><span data-stu-id="a114a-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="a114a-106">Il file con estensione msp deve includere una trasformazione che aggiunge questa proprietà alla [tabella delle proprietà](property-table.md) e ne imposta il valore.</span><span class="sxs-lookup"><span data-stu-id="a114a-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="a114a-107">Il programma di installazione scrive quindi il valore di **PATCHNEWSUMMARYCOMMENTS** nella proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="a114a-107">The installer then writes the value of **PATCHNEWSUMMARYCOMMENTS** to the [**Revision Number Summary**](revision-number-summary.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="a114a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a114a-108">Remarks</span></span>

<span data-ttu-id="a114a-109">Le proprietà [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS** e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) vengono utilizzate per aggiornare le informazioni di riepilogo quando una patch viene installata in un'immagine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="a114a-109">The [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS**, and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="a114a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a114a-110">Requirements</span></span>



| <span data-ttu-id="a114a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a114a-111">Requirement</span></span> | <span data-ttu-id="a114a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a114a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a114a-113">Versione</span><span class="sxs-lookup"><span data-stu-id="a114a-113">Version</span></span><br/> | <span data-ttu-id="a114a-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a114a-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a114a-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a114a-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a114a-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a114a-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a114a-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a114a-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a114a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a114a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a114a-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a114a-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




