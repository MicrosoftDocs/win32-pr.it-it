---
description: ICE66 utilizza le tabelle nel database per determinare lo schema che deve essere utilizzato dal database.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753015"
---
# <a name="ice66"></a><span data-ttu-id="044fe-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="044fe-103">ICE66</span></span>

<span data-ttu-id="044fe-104">ICE66 utilizza le tabelle nel database per determinare lo schema che deve essere utilizzato dal database.</span><span class="sxs-lookup"><span data-stu-id="044fe-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="044fe-105">Alcune funzionalità possono essere disponibili solo se il pacchetto viene installato in un sistema con una versione di Windows Installer corrente.</span><span class="sxs-lookup"><span data-stu-id="044fe-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="044fe-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="044fe-106">Result</span></span>

<span data-ttu-id="044fe-107">ICE66 pubblica un avviso se il database utilizza uno schema errato.</span><span class="sxs-lookup"><span data-stu-id="044fe-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="044fe-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="044fe-108">Example</span></span>

<span data-ttu-id="044fe-109">ICE66 segnala l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="044fe-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="044fe-110">Questo avviso può essere ignorato se si desidera che il pacchetto venga installato utilizzando una versione di Windows Installer corrente.</span><span class="sxs-lookup"><span data-stu-id="044fe-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="044fe-111">Se ad esempio si desidera che il pacchetto sia installabile solo nella versione 2,0 o successive, modificare lo schema del pacchetto (PID \_ PageCount) in 200.</span><span class="sxs-lookup"><span data-stu-id="044fe-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="044fe-112">Tabella IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="044fe-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="044fe-113">Componente \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="044fe-113">Component\_Shared</span></span> | <span data-ttu-id="044fe-114">\_Applicazione componente</span><span class="sxs-lookup"><span data-stu-id="044fe-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="044fe-115">Component1</span><span class="sxs-lookup"><span data-stu-id="044fe-115">Component1</span></span>        | <span data-ttu-id="044fe-116">Component2</span><span class="sxs-lookup"><span data-stu-id="044fe-116">Component2</span></span>             |



 

[<span data-ttu-id="044fe-117">Flusso di informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="044fe-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="044fe-118">PIDt</span><span class="sxs-lookup"><span data-stu-id="044fe-118">PIDt</span></span>           | <span data-ttu-id="044fe-119">Valore</span><span class="sxs-lookup"><span data-stu-id="044fe-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="044fe-120">\_PageCount PID</span><span class="sxs-lookup"><span data-stu-id="044fe-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="044fe-121">100</span><span class="sxs-lookup"><span data-stu-id="044fe-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="044fe-122">Tabella utilizzata durante l'esecuzione:</span><span class="sxs-lookup"><span data-stu-id="044fe-122">Table used during execution:</span></span>

[<span data-ttu-id="044fe-123">\_Tabella colonne</span><span class="sxs-lookup"><span data-stu-id="044fe-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="044fe-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="044fe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="044fe-125">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="044fe-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



