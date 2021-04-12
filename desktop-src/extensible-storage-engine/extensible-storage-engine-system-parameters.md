---
description: 'Altre informazioni su: parametri di sistema Extensible Storage Engine'
title: Parametri di sistema Extensible Storage Engine
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527990"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="036a6-103">Parametri di sistema Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="036a6-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="036a6-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="036a6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="036a6-105">Parametri di sistema Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="036a6-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="036a6-106">Le costanti seguenti vengono usate come valori per il parametro *Paramid* delle funzioni [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="036a6-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="036a6-107">Parametri di backup e ripristino</span><span class="sxs-lookup"><span data-stu-id="036a6-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="036a6-108">Parametri di callback</span><span class="sxs-lookup"><span data-stu-id="036a6-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="036a6-109">Parametri del database</span><span class="sxs-lookup"><span data-stu-id="036a6-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="036a6-110">Parametri della cache del database</span><span class="sxs-lookup"><span data-stu-id="036a6-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="036a6-111">Parametri di gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="036a6-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="036a6-112">Parametri del registro eventi</span><span class="sxs-lookup"><span data-stu-id="036a6-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="036a6-113">Parametri di I/O</span><span class="sxs-lookup"><span data-stu-id="036a6-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="036a6-114">Parametri dell'indice</span><span class="sxs-lookup"><span data-stu-id="036a6-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="036a6-115">Parametri informativi</span><span class="sxs-lookup"><span data-stu-id="036a6-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="036a6-116">Meta parametri</span><span class="sxs-lookup"><span data-stu-id="036a6-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="036a6-117">Parametri delle risorse</span><span class="sxs-lookup"><span data-stu-id="036a6-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="036a6-118">Parametri di database temporanei</span><span class="sxs-lookup"><span data-stu-id="036a6-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="036a6-119">Parametri del log delle transazioni</span><span class="sxs-lookup"><span data-stu-id="036a6-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="036a6-120">Formato Descrizione parametro di sistema</span><span class="sxs-lookup"><span data-stu-id="036a6-120">System Parameter Description Format</span></span>

<span data-ttu-id="036a6-121">Ogni parametro di sistema verrà descritto utilizzando il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="036a6-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="036a6-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="036a6-122">JET_paramX</span></span>

<span data-ttu-id="036a6-123">Descrizione del parametro di sistema JET_paramX.</span><span class="sxs-lookup"><span data-stu-id="036a6-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="036a6-124">Valore predefinito:</span><span class="sxs-lookup"><span data-stu-id="036a6-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="036a6-125">Valore predefinito del parametro.</span><span class="sxs-lookup"><span data-stu-id="036a6-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036a6-126">Digitare:</span><span class="sxs-lookup"><span data-stu-id="036a6-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="036a6-127">Tipo di dati del parametro.</span><span class="sxs-lookup"><span data-stu-id="036a6-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036a6-128">Intervallo valido:</span><span class="sxs-lookup"><span data-stu-id="036a6-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="036a6-129">Valori validi per il parametro.</span><span class="sxs-lookup"><span data-stu-id="036a6-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036a6-130">Ambito:</span><span class="sxs-lookup"><span data-stu-id="036a6-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="036a6-131">Il parametro è globale o per istanza?</span><span class="sxs-lookup"><span data-stu-id="036a6-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036a6-132">Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="036a6-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="036a6-133">È possibile impostare il parametro se esistono istanze?</span><span class="sxs-lookup"><span data-stu-id="036a6-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036a6-134">Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="036a6-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="036a6-135">È possibile impostare il parametro durante l'inizializzazione?</span><span class="sxs-lookup"><span data-stu-id="036a6-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036a6-136">Influiscono sul layout fisico:</span><span class="sxs-lookup"><span data-stu-id="036a6-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="036a6-137">Il parametro influisce sui file su disco?</span><span class="sxs-lookup"><span data-stu-id="036a6-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036a6-138">Influire sull'affidabilità:</span><span class="sxs-lookup"><span data-stu-id="036a6-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="036a6-139">Il parametro influisce sull'affidabilità del motore?</span><span class="sxs-lookup"><span data-stu-id="036a6-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036a6-140">Influire sulle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="036a6-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="036a6-141">Il parametro influisce sulle prestazioni del motore?</span><span class="sxs-lookup"><span data-stu-id="036a6-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="036a6-142">Influiscono sulle risorse:</span><span class="sxs-lookup"><span data-stu-id="036a6-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="036a6-143">Il parametro influisce sulle risorse del motore?</span><span class="sxs-lookup"><span data-stu-id="036a6-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="036a6-144">Disponibilità:</span><span class="sxs-lookup"><span data-stu-id="036a6-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="036a6-145">Versioni di Windows che supportano il parametro.</span><span class="sxs-lookup"><span data-stu-id="036a6-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
