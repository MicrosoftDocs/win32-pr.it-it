---
description: Il valore della proprietà ADDDEFAULT è un elenco di funzionalità delimitate da virgole, che devono essere installate nella configurazione predefinita.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Proprietà ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326053"
---
# <a name="adddefault-property"></a><span data-ttu-id="3ef23-103">Proprietà ADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="3ef23-103">ADDDEFAULT property</span></span>

<span data-ttu-id="3ef23-104">Il valore della proprietà **AddDefault** è un elenco di funzionalità delimitate da virgole, che devono essere installate nella configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3ef23-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="3ef23-105">Le funzionalità devono essere presenti nella colonna funzionalità della tabella delle [funzionalità.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="3ef23-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="3ef23-106">Per installare tutte le funzionalità nelle configurazioni predefinite, usare ADDDEFAULT = ALL nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3ef23-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="3ef23-107">Una funzionalità elencata nella proprietà **AddDefault** viene installata nello stesso stato di installazione di se l'utente ha richiesto un'installazione su richiesta della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3ef23-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="3ef23-108">Lo stato è determinato dai bit impostati per la funzionalità nella colonna attributi della [tabella delle funzionalità](feature-table.md)e dai bit impostati per i componenti della funzionalità nella colonna attributi della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3ef23-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ef23-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ef23-109">Remarks</span></span>

<span data-ttu-id="3ef23-110">I nomi delle funzionalità fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="3ef23-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="3ef23-111">Il programma di installazione valuta sempre le seguenti proprietà nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="3ef23-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="3ef23-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3ef23-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="3ef23-113">**RIMUOVERE**</span><span class="sxs-lookup"><span data-stu-id="3ef23-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="3ef23-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3ef23-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="3ef23-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3ef23-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="3ef23-116">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="3ef23-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="3ef23-117">**PUBBLICIZZARE**</span><span class="sxs-lookup"><span data-stu-id="3ef23-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="3ef23-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3ef23-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="3ef23-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3ef23-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="3ef23-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3ef23-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="3ef23-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="3ef23-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="3ef23-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="3ef23-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="3ef23-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3ef23-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="3ef23-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="3ef23-124">For example:</span></span>

-   <span data-ttu-id="3ef23-125">Se la riga di comando specifica: ADDLOCAL = ALL, ADDSOURCE = funzionalità, tutte le funzionalità vengono prima impostate su run-local, quindi la **funzionalità** è impostata su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="3ef23-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="3ef23-126">Se la riga di comando è: ADDSOURCE = ALL, ADDLOCAL = la funzionalità, First **funzionalità** è impostata su run-local e quindi quando viene valutato addsource = all, tutte le funzionalità (inclusa la **funzionalità**) vengono reimpostate su Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="3ef23-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="3ef23-127">Il programma di installazione imposta la proprietà [**preselezionata**](preselected.md) sul valore "1" durante la ripresa di un'installazione sospesa o quando una delle proprietà sopra indicate viene specificata nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3ef23-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef23-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ef23-128">Requirements</span></span>



| <span data-ttu-id="3ef23-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef23-129">Requirement</span></span> | <span data-ttu-id="3ef23-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3ef23-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef23-131">Versione</span><span class="sxs-lookup"><span data-stu-id="3ef23-131">Version</span></span><br/> | <span data-ttu-id="3ef23-132">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3ef23-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3ef23-133">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3ef23-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3ef23-134">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3ef23-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3ef23-135">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3ef23-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ef23-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ef23-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef23-137">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ef23-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




