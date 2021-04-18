---
title: Ricerca di file
description: Per impostazione predefinita, RC Cerca i file di intestazione e i file di risorse (ad esempio, i file di icona e di cursore) nella directory corrente e quindi nelle directory specificate dalla variabile di ambiente INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298631"
---
# <a name="searching-for-files"></a><span data-ttu-id="263e4-103">Ricerca di file</span><span class="sxs-lookup"><span data-stu-id="263e4-103">Searching for Files</span></span>

<span data-ttu-id="263e4-104">Per impostazione predefinita, RC Cerca i file di intestazione e i file di risorse (ad esempio, i file di icona e di cursore) nella directory corrente e quindi nelle directory specificate dalla variabile di ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="263e4-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="263e4-105">La variabile di ambiente PATH non ha alcun effetto sulle ricerche nelle directory RC.</span><span class="sxs-lookup"><span data-stu-id="263e4-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="263e4-106">Aggiunta di una directory in cui eseguire la ricerca</span><span class="sxs-lookup"><span data-stu-id="263e4-106">Adding a Directory to Search</span></span>

<span data-ttu-id="263e4-107">È possibile usare l'opzione **/i** per aggiungere una directory all'elenco di ricerche di directory RC.</span><span class="sxs-lookup"><span data-stu-id="263e4-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="263e4-108">Il compilatore cerca quindi le directory nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="263e4-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="263e4-109">Directory corrente</span><span class="sxs-lookup"><span data-stu-id="263e4-109">The current directory</span></span>
2.  <span data-ttu-id="263e4-110">La directory o le directory specificate usando l'opzione **/i** nell'ordine in cui sono visualizzate nella riga di comando RC</span><span class="sxs-lookup"><span data-stu-id="263e4-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="263e4-111">Elenco di directory specificate dalla variabile di ambiente INCLUDE, nell'ordine in cui sono elencate dalla variabile, a meno che non si specifichi l'opzione **/x**</span><span class="sxs-lookup"><span data-stu-id="263e4-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="263e4-112">Nell'esempio seguente viene compilato il file di definizione delle risorse MyApp. RC:</span><span class="sxs-lookup"><span data-stu-id="263e4-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="263e4-113">**RC/i c: \\ origine-elementi \\ /i d: \\ Resources MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="263e4-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="263e4-114">Quando si compila lo script MyApp. RC, RC cerca prima i file di intestazione e i file di risorse nella directory corrente, quindi in C: \\ source \\ Stuff e D: \\ Resources, quindi nelle directory specificate dalla variabile di ambiente include.</span><span class="sxs-lookup"><span data-stu-id="263e4-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="263e4-115">La variabile di ambiente INCLUDE verrà ignorata</span><span class="sxs-lookup"><span data-stu-id="263e4-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="263e4-116">È possibile impedire a RC di usare la variabile di ambiente INCLUDE quando si determinano le directory in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="263e4-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="263e4-117">A tale scopo, usare l'opzione **/x** .</span><span class="sxs-lookup"><span data-stu-id="263e4-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="263e4-118">Il compilatore cerca quindi i file solo nella directory corrente e in tutte le directory specificate usando l'opzione **/i** .</span><span class="sxs-lookup"><span data-stu-id="263e4-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="263e4-119">Il comando seguente compila il file script MyApp. RC:</span><span class="sxs-lookup"><span data-stu-id="263e4-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="263e4-120">**RC/x/i c: \\ materiale di origine \\ MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="263e4-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="263e4-121">Quando si compila lo script MyApp. RC, RC Cerca i file di intestazione e i file di risorse prima nella directory corrente e quindi in C: \\ source \\ Stuff.</span><span class="sxs-lookup"><span data-stu-id="263e4-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="263e4-122">Non esegue la ricerca nelle directory specificate dalla variabile di ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="263e4-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




