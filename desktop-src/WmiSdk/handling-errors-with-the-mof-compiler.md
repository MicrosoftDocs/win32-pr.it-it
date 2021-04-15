---
description: Se il compilatore MOF non è in grado di completare la compilazione di un file MOF, è possibile che il repository WMI rimanga in uno stato non definito.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Gestione degli errori con il compilatore MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485820"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="d4a0a-103">Gestione degli errori con il compilatore MOF</span><span class="sxs-lookup"><span data-stu-id="d4a0a-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="d4a0a-104">Se il compilatore MOF non è in grado di completare la compilazione di un file MOF, è possibile che il repository WMI rimanga in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="d4a0a-105">Se, ad esempio, si compila un file MOF e si usa l'opzione della riga di comando **-Class: createonly** , la compilazione termina se esiste già una classe specificata nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="d4a0a-106">Il compilatore MOF archivia nel repository tutte le classi o istanze che sono state definite fino al punto in cui si interrompe il compilatore.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="d4a0a-107">In alcuni casi, è possibile lasciare il repository WMI in una condizione non definita.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="d4a0a-108">In questa situazione, potrebbe essere necessario arrestare WMI, eliminare il repository WMI e ricompilarlo tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="d4a0a-109">Quando WMI viene riavviato, tutti i file MOF che contengono il comando [**pragma autocover**](pragma-autorecover.md) [preprocessore](preprocessor-commands.md) vengono ricompilati.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="d4a0a-110">È necessario ricompilare manualmente tutti i file MOF che non includono un' `#pragma autorecover` istruzione.</span><span class="sxs-lookup"><span data-stu-id="d4a0a-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="d4a0a-111">Per ulteriori informazioni su come dichiarare classi e istanze utilizzando la sintassi MOF, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="d4a0a-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4a0a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d4a0a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a0a-113">Compilazione di file MOF</span><span class="sxs-lookup"><span data-stu-id="d4a0a-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="d4a0a-114">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="d4a0a-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="d4a0a-115">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="d4a0a-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



