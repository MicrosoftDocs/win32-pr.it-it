---
title: Utilizzo di C/C++-preprocessore con MIDL
description: Il compilatore MIDL non esegue la pre-elaborazione dei file di origine.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL compilatore MIDL, C-preprocessore
- MIDL per il preprocessore C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329564"
---
# <a name="using-cc-preprocessor-with-midl"></a><span data-ttu-id="79a6b-105">Utilizzo di C/C++-preprocessore con MIDL</span><span class="sxs-lookup"><span data-stu-id="79a6b-105">Using C/C++-Preprocessor with MIDL</span></span>

<span data-ttu-id="79a6b-106">Il compilatore MIDL non esegue la pre-elaborazione dei file di origine.</span><span class="sxs-lookup"><span data-stu-id="79a6b-106">The MIDL compiler does not preprocess source files.</span></span> <span data-ttu-id="79a6b-107">Il compilatore MIDL usa invece un preprocessore disponibile per preparare il flusso di input per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="79a6b-107">Rather, the MIDL compiler uses an available preprocessor to prepare the input stream for parsing.</span></span> <span data-ttu-id="79a6b-108">Per impostazione predefinita, MIDL usa il preprocessore per il compilatore Microsoft C/C++ dallo stesso ambiente di compilazione di MIDL.</span><span class="sxs-lookup"><span data-stu-id="79a6b-108">By default, MIDL uses the preprocessor for the Microsoft C/C++ compiler from the same building environment as MIDL.</span></span> <span data-ttu-id="79a6b-109">Se necessario, l'utente può indicare un preprocessore diverso che verrà usato da MIDL.</span><span class="sxs-lookup"><span data-stu-id="79a6b-109">The user can indicate a different preprocessor to be used by MIDL, if needed.</span></span>

<span data-ttu-id="79a6b-110">MIDL genera esecuzioni del preprocessore separate per i file IDL e ACF di primo livello e per ogni file importato con la direttiva di importazione MIDL.</span><span class="sxs-lookup"><span data-stu-id="79a6b-110">MIDL spawns separate preprocessor runs for top-level IDL and ACF files, and for each file imported with the MIDL import directive.</span></span> <span data-ttu-id="79a6b-111">I file inclusi con la direttiva **\# include** vengono gestiti direttamente dal preprocessore.</span><span class="sxs-lookup"><span data-stu-id="79a6b-111">Files included with the **\#include** directive are handled by the preprocessor directly.</span></span>

<span data-ttu-id="79a6b-112">Negli argomenti seguenti vengono descritti i vari aspetti delle interazioni del preprocessore MIDL:</span><span class="sxs-lookup"><span data-stu-id="79a6b-112">The following topics describe various aspects of MIDL-preprocessor interactions:</span></span>

-   [<span data-ttu-id="79a6b-113">C-requisiti per il preprocessore MIDL</span><span class="sxs-lookup"><span data-stu-id="79a6b-113">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="79a6b-114">Verifica delle opzioni del preprocessore</span><span class="sxs-lookup"><span data-stu-id="79a6b-114">Verifying Preprocessor Options</span></span>](verifying-preprocessor-options.md)
-   [<span data-ttu-id="79a6b-115">Salvataggio dell'output del preprocessore</span><span class="sxs-lookup"><span data-stu-id="79a6b-115">Saving Preprocessor Output</span></span>](saving-preprocessor-output.md)
-   [<span data-ttu-id="79a6b-116">Gestione delle \# definizioni nei file IDL</span><span class="sxs-lookup"><span data-stu-id="79a6b-116">Dealing with \#defines in IDL Files</span></span>](dealing-with-defines-in-idl-files-2.md)

 

 




