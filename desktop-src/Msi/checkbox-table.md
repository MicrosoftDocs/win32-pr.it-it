---
description: La tabella CheckBox elenca i valori per le caselle di controllo.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabella CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310987"
---
# <a name="checkbox-table"></a><span data-ttu-id="0d3e0-103">Tabella CheckBox</span><span class="sxs-lookup"><span data-stu-id="0d3e0-103">CheckBox Table</span></span>

<span data-ttu-id="0d3e0-104">La tabella CheckBox elenca i valori per le caselle di controllo.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="0d3e0-105">La tabella CheckBox contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="0d3e0-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="0d3e0-106">Column</span></span>   | <span data-ttu-id="0d3e0-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d3e0-107">Type</span></span>                         | <span data-ttu-id="0d3e0-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="0d3e0-108">Key</span></span> | <span data-ttu-id="0d3e0-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="0d3e0-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="0d3e0-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d3e0-110">Property</span></span> | [<span data-ttu-id="0d3e0-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="0d3e0-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d3e0-112">S</span><span class="sxs-lookup"><span data-stu-id="0d3e0-112">Y</span></span>   | <span data-ttu-id="0d3e0-113">N</span><span class="sxs-lookup"><span data-stu-id="0d3e0-113">N</span></span>        |
| <span data-ttu-id="0d3e0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="0d3e0-114">Value</span></span>    | [<span data-ttu-id="0d3e0-115">Formattato</span><span class="sxs-lookup"><span data-stu-id="0d3e0-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="0d3e0-116">N</span><span class="sxs-lookup"><span data-stu-id="0d3e0-116">N</span></span>   | <span data-ttu-id="0d3e0-117">S</span><span class="sxs-lookup"><span data-stu-id="0d3e0-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0d3e0-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="0d3e0-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0d3e0-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d3e0-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="0d3e0-120">Proprietà denominata da associare a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="0d3e0-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="0d3e0-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="0d3e0-122">Stringa del valore associata a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d3e0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d3e0-123">Remarks</span></span>

<span data-ttu-id="0d3e0-124">Se la casella di controllo è selezionata, la proprietà corrispondente viene impostata sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="0d3e0-125">Se non è stato specificato alcun valore o la tabella non esiste, la proprietà viene impostata sul valore originale quando la casella di controllo è selezionata.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="0d3e0-126">Se il valore originale è null, la proprietà viene impostata su "1".</span><span class="sxs-lookup"><span data-stu-id="0d3e0-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="0d3e0-127">Il contenuto della colonna valore viene formattato in base alla funzione [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando viene creato il controllo.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="0d3e0-128">Può quindi contenere qualsiasi espressione che la funzione **MsiFormatRecord** può interpretare.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="0d3e0-129">La colonna valore viene formattata solo quando il controllo viene creato e non viene aggiornata se una proprietà in un'espressione viene modificata durante il ciclo di vita del controllo.</span><span class="sxs-lookup"><span data-stu-id="0d3e0-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="0d3e0-130">Convalida</span><span class="sxs-lookup"><span data-stu-id="0d3e0-130">Validation</span></span>

<dl>

[<span data-ttu-id="0d3e0-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="0d3e0-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0d3e0-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="0d3e0-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0d3e0-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="0d3e0-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



