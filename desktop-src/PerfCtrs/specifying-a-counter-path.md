---
description: Il sistema usa i contatori per raccogliere i dati sulle prestazioni.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Specifying a Counter Path (Specifica di un percorso di contatore)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312084"
---
# <a name="specifying-a-counter-path"></a><span data-ttu-id="d8614-103">Specifying a Counter Path (Specifica di un percorso di contatore)</span><span class="sxs-lookup"><span data-stu-id="d8614-103">Specifying a Counter Path</span></span>

<span data-ttu-id="d8614-104">Il sistema usa i contatori per raccogliere i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d8614-104">The system uses counters to collect performance data.</span></span> <span data-ttu-id="d8614-105">Ogni contatore viene identificato in modo univoco tramite il nome, il percorso o il percorso.</span><span class="sxs-lookup"><span data-stu-id="d8614-105">Each counter is uniquely identified through its name and its path, or location.</span></span> <span data-ttu-id="d8614-106">La sintassi di un percorso del contatore è:</span><span class="sxs-lookup"><span data-stu-id="d8614-106">The syntax of a counter path is:</span></span>

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

<span data-ttu-id="d8614-107">L'elemento computer specifica il nome o l'indirizzo IP del computer da cui si desidera eseguire una query sui dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d8614-107">The Computer element specifies the name or IP address of the computer from which you want to query performance data.</span></span> <span data-ttu-id="d8614-108">Il nome del computer è facoltativo se il contatore si trova nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d8614-108">The computer name is optional if the counter is located on the local computer.</span></span>

<span data-ttu-id="d8614-109">L'elemento PerfObject specifica l'oggetto prestazione su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="d8614-109">The PerfObject element specifies the performance object to query.</span></span> <span data-ttu-id="d8614-110">Un oggetto prestazione può essere un componente fisico, ad esempio processori, dischi e memoria, oppure un oggetto di sistema, ad esempio processi e thread.</span><span class="sxs-lookup"><span data-stu-id="d8614-110">A performance object can be a physical component, such as processors, disks, and memory, or a system object, such as processes and threads.</span></span> <span data-ttu-id="d8614-111">Ogni oggetto di sistema è correlato a un elemento funzionale all'interno del computer ed è associato a un set di contatori standard.</span><span class="sxs-lookup"><span data-stu-id="d8614-111">Each system object is related to a functional element within the computer and has a set of standard counters assigned to it.</span></span> <span data-ttu-id="d8614-112">Ogni computer potrebbe disporre di un set diverso di oggetti prestazioni e di contatori installati, perché le applicazioni possono installare gli oggetti e i contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d8614-112">Each computer may have a different set of performance objects and counters installed on it because applications can install their own performance objects and counters.</span></span> <span data-ttu-id="d8614-113">Per un elenco degli oggetti e dei contatori delle prestazioni installati nel computer, vedere la finestra di dialogo **Aggiungi contatori** nello strumento prestazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="d8614-113">For a list of the performance objects and counters installed on your computer, see the **Add Counters** dialog box in the Performance tool on your computer.</span></span> <span data-ttu-id="d8614-114">Questi oggetti sono elencati anche nella finestra di dialogo PDH Browse (vedere l' [esplorazione dei contatori](browsing-counters.md)).</span><span class="sxs-lookup"><span data-stu-id="d8614-114">These objects are also listed in the PDH browse dialog box (see [Browsing Counters](browsing-counters.md)).</span></span> <span data-ttu-id="d8614-115">Per un elenco degli oggetti e dei contatori delle prestazioni di sistema, vedere [contatori per oggetto](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d8614-115">For a list of system performance objects and counters, see [Counters by Object](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).</span></span>

<span data-ttu-id="d8614-116">ParentInstance, ObjectInstance e InstanceIndex sono inclusi nel percorso se possono esistere più istanze dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d8614-116">The ParentInstance, ObjectInstance, and InstanceIndex are included in the path if multiple instances of the object can exist.</span></span> <span data-ttu-id="d8614-117">I processi e i thread, ad esempio, sono più oggetti istanza perché possono essere eseguiti contemporaneamente più processi o thread.</span><span class="sxs-lookup"><span data-stu-id="d8614-117">For example, processes and threads are multiple instance objects because more than one process or thread can run at the same time.</span></span> <span data-ttu-id="d8614-118">Se un oggetto può avere più di un'istanza, è necessario che il percorso del contatore specifichi un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d8614-118">If an object can have more than one instance, the counter path must specify an object instance.</span></span>

<span data-ttu-id="d8614-119">Il formato degli elementi correlati all'istanza dipende dal tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="d8614-119">The format of the instance related elements depends on the object type.</span></span> <span data-ttu-id="d8614-120">Se l'oggetto dispone di istanze semplici, il formato è solo il nome dell'istanza racchiuso tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="d8614-120">If the object has simple instances, then the format is only the instance name enclosed in parentheses.</span></span> <span data-ttu-id="d8614-121">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d8614-121">For example:</span></span>

``` syntax
(Explorer)
```

<span data-ttu-id="d8614-122">Se l'istanza di questo oggetto richiede anche un nome di istanza padre, il nome dell'istanza padre deve precedere l'istanza dell'oggetto ed essere separato da un carattere di barra.</span><span class="sxs-lookup"><span data-stu-id="d8614-122">If the instance of this object also requires a parent instance name, the parent instance name must come before the object instance and be separated by a forward slash character.</span></span> <span data-ttu-id="d8614-123">Ad esempio, i thread appartengono ai processi.</span><span class="sxs-lookup"><span data-stu-id="d8614-123">For example, threads belong to processes.</span></span> <span data-ttu-id="d8614-124">Se si esegue una query su un oggetto thread, è necessario specificare anche il processo a cui appartiene, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d8614-124">If you query a thread object, you must also specify the process to which it belongs as shown in the following example:</span></span>

``` syntax
(Explorer/0)
```

<span data-ttu-id="d8614-125">Se l'oggetto dispone di più istanze con la stessa stringa del nome, è possibile indicizzarle in modo sequenziale specificando l'indice dell'istanza preceduto da un segno di cancelletto.</span><span class="sxs-lookup"><span data-stu-id="d8614-125">If the object has multiple instances that have the same name string, they can be indexed sequentially by specifying the instance index prefixed by a pound sign.</span></span> <span data-ttu-id="d8614-126">Gli indici di istanza sono basati su 0.</span><span class="sxs-lookup"><span data-stu-id="d8614-126">Instance indexes are 0-based.</span></span> <span data-ttu-id="d8614-127">Se si desidera eseguire una query sulla prima istanza, non includere \# 0, ma è sufficiente specificare il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d8614-127">If you want to query the first instance, do not include \#0—just specify the instance name.</span></span> <span data-ttu-id="d8614-128">Per specificare la seconda istanza, utilizzare \# 1. per specificare la terza istanza, utilizzare \# 2 e così via.</span><span class="sxs-lookup"><span data-stu-id="d8614-128">To specify the second instance, use \#1; to specify the third instance, use \#2; and so on.</span></span> <span data-ttu-id="d8614-129">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d8614-129">For example:</span></span>

``` syntax
(Explorer/0#1)
```

<span data-ttu-id="d8614-130">L'elemento contatore specifica il contatore delle prestazioni su cui si desidera eseguire una query per l'oggetto prestazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d8614-130">The Counter element specifies the performance counter that you want to query for the given the performance object.</span></span>

<span data-ttu-id="d8614-131">PDH usa i caratteri speciali seguenti in un percorso del contatore.</span><span class="sxs-lookup"><span data-stu-id="d8614-131">PDH uses the following special characters in a counter path.</span></span> <span data-ttu-id="d8614-132">I provider non devono utilizzare questi caratteri nel nome.</span><span class="sxs-lookup"><span data-stu-id="d8614-132">Providers should not use these characters in their names.</span></span> <span data-ttu-id="d8614-133">Se un provider utilizza questi caratteri speciali, PDH non è in grado di analizzare il percorso completo del contatore per ottenere i nomi dei contatori e delle istanze.</span><span class="sxs-lookup"><span data-stu-id="d8614-133">If a provider uses these special characters, PDH cannot parse the full counter path to obtain the counter and instances names.</span></span>



| <span data-ttu-id="d8614-134">Carattere</span><span class="sxs-lookup"><span data-stu-id="d8614-134">Character</span></span> | <span data-ttu-id="d8614-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8614-135">Description</span></span>                                                |
|-----------|------------------------------------------------------------|
| \\        | <span data-ttu-id="d8614-136">Separatore generico per computer, oggetto e contatore.</span><span class="sxs-lookup"><span data-stu-id="d8614-136">Generic separator for computer, object, and counter.</span></span>       |
| <span data-ttu-id="d8614-137">(</span><span class="sxs-lookup"><span data-stu-id="d8614-137">(</span></span>         | <span data-ttu-id="d8614-138">Inizio del nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d8614-138">Beginning of instance name.</span></span>                                |
| <span data-ttu-id="d8614-139">)</span><span class="sxs-lookup"><span data-stu-id="d8614-139">)</span></span>         | <span data-ttu-id="d8614-140">Fine del nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d8614-140">Ending of instance name.</span></span>                                   |
| /         | <span data-ttu-id="d8614-141">Separa l'istanza e l'istanza padre.</span><span class="sxs-lookup"><span data-stu-id="d8614-141">Separates instance and parent instance.</span></span>                    |
| <span data-ttu-id="d8614-142">\#n</span><span class="sxs-lookup"><span data-stu-id="d8614-142">\#n</span></span>       | <span data-ttu-id="d8614-143">Identifica un'occorrenza specifica di un'istanza con nome uguale.</span><span class="sxs-lookup"><span data-stu-id="d8614-143">Identifies a specific occurrence of a same-named instance.</span></span> |
| \*        | <span data-ttu-id="d8614-144">Carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="d8614-144">Wildcard character.</span></span>                                        |



 

<span data-ttu-id="d8614-145">Negli esempi seguenti vengono illustrati i formati possibili per i percorsi dei contatori:</span><span class="sxs-lookup"><span data-stu-id="d8614-145">The following examples show the possible formats for counter paths:</span></span>

-   <span data-ttu-id="d8614-146">\\\\\\contatore oggetto computer (indice padre/istanza \# ) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-146">\\\\computer\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="d8614-147">\\\\\\contatore oggetto computer (padre/istanza) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-147">\\\\computer\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="d8614-148">\\\\\\contatore oggetto computer ( \# Indice istanza) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-148">\\\\computer\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="d8614-149">\\\\\\contatore oggetto computer (istanza) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-149">\\\\computer\\object(instance)\\counter</span></span>
-   <span data-ttu-id="d8614-150">\\\\\\contatore oggetto \\ computer</span><span class="sxs-lookup"><span data-stu-id="d8614-150">\\\\computer\\object\\counter</span></span>
-   <span data-ttu-id="d8614-151">\\contatore oggetto (indice padre/istanza \# ) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-151">\\object(parent/instance\#index)\\counter</span></span>
-   <span data-ttu-id="d8614-152">\\contatore oggetto (padre/istanza) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-152">\\object(parent/instance)\\counter</span></span>
-   <span data-ttu-id="d8614-153">\\contatore oggetto ( \# Indice istanza) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-153">\\object(instance\#index)\\counter</span></span>
-   <span data-ttu-id="d8614-154">\\contatore oggetto (istanza) \\</span><span class="sxs-lookup"><span data-stu-id="d8614-154">\\object(instance)\\counter</span></span>
-   <span data-ttu-id="d8614-155">\\\\contatore oggetti</span><span class="sxs-lookup"><span data-stu-id="d8614-155">\\object\\counter</span></span>

## <a name="using-wildcard-characters"></a><span data-ttu-id="d8614-156">Utilizzo di caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="d8614-156">Using wildcard characters</span></span>

<span data-ttu-id="d8614-157">I percorsi dei contatori possono contenere un carattere jolly solo per il nome dell'istanza, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d8614-157">Counter paths may contain a wildcard character only for the instance name as shown in the following example.</span></span>

``` syntax
\Process(*)\% Processor Time
```

<span data-ttu-id="d8614-158">Per espandere il carattere jolly in un elenco di percorsi dei contatori contenenti le istanze trovate nel computer o nel file di log, chiamare [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span><span class="sxs-lookup"><span data-stu-id="d8614-158">To expand the wildcard into a list of counter paths that contain instances found on the computer or in the log file, call [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).</span></span>

 

 
