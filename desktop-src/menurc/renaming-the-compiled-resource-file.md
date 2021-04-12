---
title: Ridenominazione del file di risorse compilato
description: Per impostazione predefinita, quando si compilano risorse, RC denomina il file di risorse compilato (res) con il nome di base del file RC e lo inserisce nella stessa directory del file RC.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220985"
---
# <a name="renaming-the-compiled-resource-file"></a><span data-ttu-id="627f2-103">Ridenominazione del file di risorse compilato</span><span class="sxs-lookup"><span data-stu-id="627f2-103">Renaming the Compiled Resource File</span></span>

<span data-ttu-id="627f2-104">Per impostazione predefinita, quando si compilano risorse, RC denomina il file di risorse compilato (res) con il nome di base del file RC e lo inserisce nella stessa directory del file RC.</span><span class="sxs-lookup"><span data-stu-id="627f2-104">By default, when compiling resources, RC names the compiled resource (.res) file with the base name of the .rc file and places it in the same directory as the .rc file.</span></span> <span data-ttu-id="627f2-105">CVTRES deve quindi essere richiamato per convertire il file con estensione RES in un formato di risorsa binario (con estensione RBJ) che può essere riconosciuto dal linker.</span><span class="sxs-lookup"><span data-stu-id="627f2-105">CVTRES must then be invoked to convert the .res file to a binary resource (.rbj) format which can be understood by the linker.</span></span> <span data-ttu-id="627f2-106">Nell'esempio seguente viene compilato MyApp. RC e viene creato un file di risorse compilato denominato MyApp. res nella stessa directory di MyApp. RC:</span><span class="sxs-lookup"><span data-stu-id="627f2-106">The following example compiles MyApp.rc and creates a compiled resource file named MyApp.res in the same directory as MyApp.rc:</span></span>

<span data-ttu-id="627f2-107">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="627f2-107">**rc myapp.rc**</span></span>

<span data-ttu-id="627f2-108">L'opzione **/fo** assegna al file res risultante un nome diverso dal nome del file RC corrispondente.</span><span class="sxs-lookup"><span data-stu-id="627f2-108">The **/fo** option gives the resulting .res file a name that differs from the name of the corresponding .rc file.</span></span> <span data-ttu-id="627f2-109">Ad esempio, per assegnare un nome al file res. res risultante, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="627f2-109">For example, to name the resulting .res file NewFile.res, use the following command:</span></span>

<span data-ttu-id="627f2-110">**RC-fo NewFile. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="627f2-110">**rc -fo newfile.res myapp.rc**</span></span>

<span data-ttu-id="627f2-111">L'opzione **/fo** può anche inserire il file con estensione RES in una directory diversa.</span><span class="sxs-lookup"><span data-stu-id="627f2-111">The **/fo** option can also place the .res file in a different directory.</span></span> <span data-ttu-id="627f2-112">Il comando seguente, ad esempio, inserisce il file di risorse compilato MyApp. res nella directory C: \\ source \\ Resource:</span><span class="sxs-lookup"><span data-stu-id="627f2-112">For example, the following command places the compiled resource file MyApp.res in the directory C:\\Source\\Resource:</span></span>

<span data-ttu-id="627f2-113">**RC-fo c: \\ risorsa di origine \\ \\ MyApp. res MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="627f2-113">**rc -fo c:\\source\\resource\\myapp.res myapp.rc**</span></span>

 

 




