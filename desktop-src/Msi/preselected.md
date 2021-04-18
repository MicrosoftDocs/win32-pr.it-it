---
description: La proprietà preselezionata indica che le funzionalità sono già state selezionate e che non è necessario visualizzare la finestra di dialogo di selezione. Espressioni condizionali che variano a seconda che le funzionalità siano già installate, usare questo valore.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Proprietà preselezionata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331608"
---
# <a name="preselected-property"></a><span data-ttu-id="e0fea-103">Proprietà preselezionata</span><span class="sxs-lookup"><span data-stu-id="e0fea-103">Preselected property</span></span>

<span data-ttu-id="e0fea-104">La proprietà **preselezionata** indica che le funzionalità sono già state selezionate e che non è necessario visualizzare la finestra di dialogo di selezione.</span><span class="sxs-lookup"><span data-stu-id="e0fea-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="e0fea-105">Espressioni condizionali che variano a seconda che le funzionalità siano già installate, usare questo valore.</span><span class="sxs-lookup"><span data-stu-id="e0fea-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="e0fea-106">La proprietà, ad esempio, può essere utilizzata per disattivare eventuali finestre di dialogo che coinvolgono le selezioni di funzionalità durante la ripresa di un'installazione sospesa.</span><span class="sxs-lookup"><span data-stu-id="e0fea-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="e0fea-107">Il programma di installazione imposta la proprietà **preselezionata** sul valore "1" durante la ripresa di un'installazione sospesa o quando nella riga di comando viene specificata una delle proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0fea-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="e0fea-108">Se la proprietà **preselezionata** è stata impostata su 1, il programma di installazione non utilizza la [tabella della condizione](condition-table.md) per valutare la selezione delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e0fea-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="e0fea-109">Le funzionalità vengono installate in base alle proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0fea-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="e0fea-110">Il programma di installazione valuta sempre queste proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="e0fea-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="e0fea-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="e0fea-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="e0fea-112">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="e0fea-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="e0fea-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="e0fea-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="e0fea-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e0fea-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="e0fea-115">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="e0fea-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="e0fea-116">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="e0fea-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="e0fea-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="e0fea-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="e0fea-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="e0fea-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="e0fea-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e0fea-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="e0fea-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="e0fea-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="e0fea-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="e0fea-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="e0fea-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e0fea-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="e0fea-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0fea-123">Requirements</span></span>



| <span data-ttu-id="e0fea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0fea-124">Requirement</span></span> | <span data-ttu-id="e0fea-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e0fea-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fea-126">Versione</span><span class="sxs-lookup"><span data-stu-id="e0fea-126">Version</span></span><br/> | <span data-ttu-id="e0fea-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e0fea-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e0fea-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0fea-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e0fea-129">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0fea-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e0fea-130">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e0fea-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0fea-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0fea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fea-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0fea-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




