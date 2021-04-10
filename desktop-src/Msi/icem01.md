---
description: ICEM01 verifica che il meccanismo ICE funzioni correttamente. Questo ghiaccio usa la proprietà Time per ottenere l'ora e restituisce l'ora di sistema o None.
ms.assetid: f3b7677d-6b2e-4aa0-92eb-1b1e62cdf0a6
title: ICEM01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca7f2ffb3fcf5e3d50a3937a1f17fddd3a912f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129959"
---
# <a name="icem01"></a><span data-ttu-id="419a3-104">ICEM01</span><span class="sxs-lookup"><span data-stu-id="419a3-104">ICEM01</span></span>

<span data-ttu-id="419a3-105">ICEM01 verifica che il meccanismo ICE funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="419a3-105">ICEM01 validates that the ICE mechanism is working.</span></span> <span data-ttu-id="419a3-106">Questo ghiaccio usa la proprietà [**Time**](time.md) per ottenere l'ora e restituisce l'ora di sistema o None.</span><span class="sxs-lookup"><span data-stu-id="419a3-106">This ICE uses the [**Time**](time.md) property to get the time and returns either the system time or None.</span></span>

<span data-ttu-id="419a3-107">I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="419a3-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="419a3-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="419a3-108">Result</span></span>

<span data-ttu-id="419a3-109">ICEM01 pubblica un messaggio che indica il momento in cui il programma di installazione ha chiamato ICEM01.</span><span class="sxs-lookup"><span data-stu-id="419a3-109">ICEM01 posts a message giving the time the installer called ICEM01.</span></span> <span data-ttu-id="419a3-110">Questo ghiaccio non dovrebbe mai restituire un errore.</span><span class="sxs-lookup"><span data-stu-id="419a3-110">This ICE should never return an error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="419a3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="419a3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="419a3-112">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="419a3-112">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



