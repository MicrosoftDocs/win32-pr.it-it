---
description: La proprietà PATCHNEWPACKAGECODE aggiorna la proprietà di riepilogo dei numeri di revisione di un'immagine amministrativa durante l'applicazione di patch.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Proprietà PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324772"
---
# <a name="patchnewpackagecode-property"></a><span data-ttu-id="d6c9d-103">Proprietà PATCHNEWPACKAGECODE</span><span class="sxs-lookup"><span data-stu-id="d6c9d-103">PATCHNEWPACKAGECODE property</span></span>

<span data-ttu-id="d6c9d-104">La proprietà **PATCHNEWPACKAGECODE** aggiorna la proprietà di [**Riepilogo dei numeri di revisione**](revision-number-summary.md) di un'immagine amministrativa durante l'applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-104">The **PATCHNEWPACKAGECODE** property updates the [**Revision Number Summary**](revision-number-summary.md) property of an administrative image during patching.</span></span> <span data-ttu-id="d6c9d-105">Questa proprietà viene impostata solo da una trasformazione in un file con estensione msp.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="d6c9d-106">Il file con estensione msp deve includere una trasformazione che aggiunge questa proprietà alla [tabella delle proprietà](property-table.md) e ne imposta il valore.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="d6c9d-107">Il programma di installazione scrive quindi il valore di **PATCHNEWPACKAGECODE** nella proprietà di **Riepilogo dei numeri di revisione** .</span><span class="sxs-lookup"><span data-stu-id="d6c9d-107">The installer then writes the value of **PATCHNEWPACKAGECODE** to the **Revision Number Summary** property.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c9d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6c9d-108">Remarks</span></span>

<span data-ttu-id="d6c9d-109">Le proprietà **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) vengono utilizzate per aggiornare le informazioni di riepilogo quando una patch viene installata in un'immagine amministrativa.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-109">The **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md), and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c9d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6c9d-110">Requirements</span></span>



| <span data-ttu-id="d6c9d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c9d-111">Requirement</span></span> | <span data-ttu-id="d6c9d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d6c9d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c9d-113">Versione</span><span class="sxs-lookup"><span data-stu-id="d6c9d-113">Version</span></span><br/> | <span data-ttu-id="d6c9d-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6c9d-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6c9d-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d6c9d-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d6c9d-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6c9d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6c9d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c9d-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d6c9d-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




