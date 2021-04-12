---
description: Se una tabella del modulo merge è elencata nella tabella ModuleIgnoreTable, non viene unita nel file con estensione msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabella ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233508"
---
# <a name="moduleignoretable-table"></a><span data-ttu-id="9593f-103">Tabella ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="9593f-103">ModuleIgnoreTable Table</span></span>

<span data-ttu-id="9593f-104">Se una tabella del modulo merge è elencata nella tabella ModuleIgnoreTable, non viene unita nel file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="9593f-104">If a table in the merge module is listed in the ModuleIgnoreTable table, it is not merged into the .msi file.</span></span> <span data-ttu-id="9593f-105">Se la tabella esiste già nel file con estensione msi, non viene modificata dall'Unione.</span><span class="sxs-lookup"><span data-stu-id="9593f-105">If the table already exists in the .msi file, it is not modified by the merge.</span></span> <span data-ttu-id="9593f-106">Le tabelle in ModuleIgnoreTable possono quindi contenere dati che non sono necessari dopo l'Unione.</span><span class="sxs-lookup"><span data-stu-id="9593f-106">The tables in the ModuleIgnoreTable can therefore contain data that is unneeded after the merge.</span></span>

<span data-ttu-id="9593f-107">La tabella ModuleIgnoreTable include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="9593f-107">The ModuleIgnoreTable table has the following columns.</span></span>



| <span data-ttu-id="9593f-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="9593f-108">Column</span></span> | <span data-ttu-id="9593f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9593f-109">Type</span></span>                         | <span data-ttu-id="9593f-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="9593f-110">Key</span></span> | <span data-ttu-id="9593f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="9593f-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="9593f-112">Tabella</span><span class="sxs-lookup"><span data-stu-id="9593f-112">Table</span></span>  | [<span data-ttu-id="9593f-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="9593f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="9593f-114">S</span><span class="sxs-lookup"><span data-stu-id="9593f-114">Y</span></span>   | <span data-ttu-id="9593f-115">No</span><span class="sxs-lookup"><span data-stu-id="9593f-115">No</span></span>       |



 

## <a name="columns"></a><span data-ttu-id="9593f-116">Colonne</span><span class="sxs-lookup"><span data-stu-id="9593f-116">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9593f-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo</span><span class="sxs-lookup"><span data-stu-id="9593f-117"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="9593f-118">Nome della tabella nel modulo merge che non deve essere sottoposta a merge nel file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="9593f-118">Name of the table in the merge module that is not to be merged into the .msi file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9593f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="9593f-119">Remarks</span></span>

<span data-ttu-id="9593f-120">Per ridurre al minimo le dimensioni del file con estensione MSM, è consigliabile che gli sviluppatori rimuovano le tabelle inutilizzate da moduli destinati alla ridistribuzione anziché elencare queste tabelle nella tabella ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="9593f-120">To minimize the size of the .msm file, it is recommended that developers remove unused tables from modules intended for redistribution rather than listing these tables in the ModuleIgnoreTable table.</span></span>

 

 



