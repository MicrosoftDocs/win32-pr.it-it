---
description: ICE45 verifica che le colonne del campo di bit nel database non impostino bit riservati su 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227197"
---
# <a name="ice45"></a><span data-ttu-id="14656-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="14656-103">ICE45</span></span>

<span data-ttu-id="14656-104">ICE45 verifica che le colonne del campo di bit nel database non impostino bit riservati su 1.</span><span class="sxs-lookup"><span data-stu-id="14656-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="14656-105">I bit riservati non forniscono funzionalità nelle versioni correnti del programma di installazione, ma potrebbero nelle versioni future.</span><span class="sxs-lookup"><span data-stu-id="14656-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="14656-106">Devono essere impostati su 0 per essere compatibili con le versioni future di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="14656-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="14656-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="14656-107">Result</span></span>

<span data-ttu-id="14656-108">ICE45 Invia un messaggio di errore se una delle tabelle seguenti contiene un campo di bit con un bit riservato impostato su un valore pari a 1.</span><span class="sxs-lookup"><span data-stu-id="14656-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="14656-109">Tabella BBControl</span><span class="sxs-lookup"><span data-stu-id="14656-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="14656-110">Tabella finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="14656-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="14656-111">Tabella delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="14656-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="14656-112">Tabella file</span><span class="sxs-lookup"><span data-stu-id="14656-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="14656-113">Tabella MoveFile</span><span class="sxs-lookup"><span data-stu-id="14656-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="14656-114">Tabella ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="14656-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="14656-115">Tabella ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="14656-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="14656-116">Tabella patch</span><span class="sxs-lookup"><span data-stu-id="14656-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="14656-117">Tabella RemoveFile</span><span class="sxs-lookup"><span data-stu-id="14656-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="14656-118">Tabella ServiceControl</span><span class="sxs-lookup"><span data-stu-id="14656-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="14656-119">Tabella ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="14656-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="14656-120">Tabella TextStyle</span><span class="sxs-lookup"><span data-stu-id="14656-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="14656-121">ICE45 invia uno dei due messaggi di avviso se la [tabella di controllo](control-table.md) contiene un campo di bit con un bit riservato impostato su un valore pari a 1.</span><span class="sxs-lookup"><span data-stu-id="14656-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="14656-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="14656-122">Example</span></span>

<span data-ttu-id="14656-123">ICE45 segnala l'errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="14656-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="14656-124">ICE45 segnala l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="14656-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="14656-125">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="14656-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="14656-126">File</span><span class="sxs-lookup"><span data-stu-id="14656-126">File</span></span>  | <span data-ttu-id="14656-127">Attributi</span><span class="sxs-lookup"><span data-stu-id="14656-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="14656-128">File1</span><span class="sxs-lookup"><span data-stu-id="14656-128">File1</span></span> | <span data-ttu-id="14656-129">128</span><span class="sxs-lookup"><span data-stu-id="14656-129">128</span></span>        |



 

<span data-ttu-id="14656-130">[Tabella di controllo](control-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="14656-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="14656-131">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="14656-131">Dialog</span></span>  | <span data-ttu-id="14656-132">Control</span><span class="sxs-lookup"><span data-stu-id="14656-132">Control</span></span> | <span data-ttu-id="14656-133">Attributi</span><span class="sxs-lookup"><span data-stu-id="14656-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="14656-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="14656-134">Dialog1</span></span> | <span data-ttu-id="14656-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="14656-135">Edit1</span></span>   | <span data-ttu-id="14656-136">2097152</span><span class="sxs-lookup"><span data-stu-id="14656-136">2097152</span></span>    |
| <span data-ttu-id="14656-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="14656-137">Dialog1</span></span> | <span data-ttu-id="14656-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="14656-138">Edit2</span></span>   | <span data-ttu-id="14656-139">1048576</span><span class="sxs-lookup"><span data-stu-id="14656-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="14656-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14656-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14656-141">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="14656-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



