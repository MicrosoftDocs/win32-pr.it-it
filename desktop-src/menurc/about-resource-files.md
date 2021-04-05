---
title: Informazioni sui file di risorse
description: Viene descritto come includere le risorse nell'applicazione basata su Windows con RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044719"
---
# <a name="about-resource-files"></a><span data-ttu-id="27ec7-103">Informazioni sui file di risorse</span><span class="sxs-lookup"><span data-stu-id="27ec7-103">About Resource Files</span></span>

<span data-ttu-id="27ec7-104">Per includere le risorse nell'applicazione basata su Windows con RC, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="27ec7-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="27ec7-105">Creare singoli file per i cursori, le icone, le bitmap, le finestre di dialogo e i tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="27ec7-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="27ec7-106">Creare uno script di definizione di risorsa (file RC) che descriva le risorse usate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27ec7-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="27ec7-107">Compilare lo script con RC.</span><span class="sxs-lookup"><span data-stu-id="27ec7-107">Compile the script with RC.</span></span> <span data-ttu-id="27ec7-108">Per altre informazioni, vedere [uso di RC (riga di comando RC)](using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="27ec7-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="27ec7-109">Collegare il file di risorse compilato (res) al file eseguibile dell'applicazione con il linker.</span><span class="sxs-lookup"><span data-stu-id="27ec7-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="27ec7-110">Un file di risorse è un file di testo con estensione RC.</span><span class="sxs-lookup"><span data-stu-id="27ec7-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="27ec7-111">Il file può utilizzare caratteri a byte singolo, a doppio byte o Unicode.</span><span class="sxs-lookup"><span data-stu-id="27ec7-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="27ec7-112">La sintassi e la semantica per il preprocessore RC sono simili a quelle del compilatore Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="27ec7-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="27ec7-113">Tuttavia, RC supporta un subset delle direttive per il preprocessore, definisce e pragma in uno script.</span><span class="sxs-lookup"><span data-stu-id="27ec7-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="27ec7-114">Il file di script definisce le risorse.</span><span class="sxs-lookup"><span data-stu-id="27ec7-114">The script file defines resources.</span></span> <span data-ttu-id="27ec7-115">Per una risorsa esistente in un file separato, ad esempio un'icona o un cursore, lo script specifica la risorsa e il file che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="27ec7-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="27ec7-116">Per alcune risorse, ad esempio un menu, l'intera definizione della risorsa è presente nello script.</span><span class="sxs-lookup"><span data-stu-id="27ec7-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="27ec7-117">Negli argomenti seguenti vengono descritte le informazioni che possono essere contenute in un file script:</span><span class="sxs-lookup"><span data-stu-id="27ec7-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="27ec7-118">[Commenti](comments.md), che sono note che devono essere ignorate da RC.</span><span class="sxs-lookup"><span data-stu-id="27ec7-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="27ec7-119">Le [macro predefinite](predefined-macros.md), che non accettano argomenti e non possono essere ridefinite.</span><span class="sxs-lookup"><span data-stu-id="27ec7-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="27ec7-120">[Direttive per il preprocessore](preprocessor-directives.md), che indicano a RC di eseguire azioni sullo script prima di compilarlo.</span><span class="sxs-lookup"><span data-stu-id="27ec7-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="27ec7-121">[Operatori del preprocessore](preprocessor-operators.md), utilizzati con la direttiva **\# define** .</span><span class="sxs-lookup"><span data-stu-id="27ec7-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="27ec7-122">Direttive pragma</span><span class="sxs-lookup"><span data-stu-id="27ec7-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="27ec7-123">[Istruzioni per la definizione delle](resource-definition-statements.md)risorse, che denominano e descrivono le risorse.</span><span class="sxs-lookup"><span data-stu-id="27ec7-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




