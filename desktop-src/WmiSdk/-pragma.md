---
description: È simile a un'opzione della riga di comando. Tuttavia, non è necessario immettere nuovamente un \# comando pragma ogni volta che si compila un file MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317581"
---
# <a name="pragma"></a><span data-ttu-id="b5ae4-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="b5ae4-104">\#pragma</span></span>

<span data-ttu-id="b5ae4-105">Il comando per il preprocessore **\# pragma** è simile a un'opzione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="b5ae4-106">Tuttavia, non è necessario immettere nuovamente un comando **\# pragma** ogni volta che si compila un file MOF.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="b5ae4-107">Nell'esempio seguente viene illustrata la sintassi del comando **\# pragma** :</span><span class="sxs-lookup"><span data-stu-id="b5ae4-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="b5ae4-108">In genere si inserisce un comando **\# pragma** all'inizio di un file MOF.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="b5ae4-109">Tuttavia, è possibile inserire alcuni comandi, ad esempio il comando **\# pragma** , nel corpo del codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="b5ae4-110">Nell'esempio seguente vengono illustrati i comandi **\# pragma** che indicano al compilatore MOF che deve inserire classi e istanze nello \\ spazio dei nomi CIMV2 radice e compilare il file in cui sono inclusi i comandi durante il ripristino del repository:</span><span class="sxs-lookup"><span data-stu-id="b5ae4-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="b5ae4-111">Di seguito sono elencati i comandi **\# pragma** disponibili.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="b5ae4-112">Comando</span><span class="sxs-lookup"><span data-stu-id="b5ae4-112">Command</span></span>                                         | <span data-ttu-id="b5ae4-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5ae4-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5ae4-114">**emendamento**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="b5ae4-115">Indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="b5ae4-116">**salvataggio automatico**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="b5ae4-117">Aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="b5ae4-118">**classFlags**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="b5ae4-119">Controlla il modo in cui le classi vengono create o aggiornate a seconda dei flag specificati.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="b5ae4-120">**deleteclass**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="b5ae4-121">Elimina una classe esistente e le relative istanze dal repository.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="b5ae4-122">**DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="b5ae4-123">Elimina un'istanza esistente di una classe dal repository.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="b5ae4-124">**instanceflags**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="b5ae4-125">Controlla il modo in cui le istanze vengono create o aggiornate a seconda dei flag specificati.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="b5ae4-126">**namespace**</span><span class="sxs-lookup"><span data-stu-id="b5ae4-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="b5ae4-127">Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacePath*.</span><span class="sxs-lookup"><span data-stu-id="b5ae4-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="b5ae4-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b5ae4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ae4-129">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="b5ae4-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



