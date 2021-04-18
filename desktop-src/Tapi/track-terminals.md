---
description: Due tipi di terminali Track sono definiti registrazione del terminale di tracking e della riproduzione, che appartengono rispettivamente a e sono gestiti dal terminale di registrazione file e dal terminale di riproduzione file.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Rileva terminali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315796"
---
# <a name="track-terminals"></a><span data-ttu-id="25207-103">Rileva terminali</span><span class="sxs-lookup"><span data-stu-id="25207-103">Track Terminals</span></span>

<span data-ttu-id="25207-104">Sono definiti due tipi di terminali di rilevamento: la registrazione di Track Terminal e playback Track Terminal, che, rispettivamente, appartengono a e sono gestiti dal terminale di registrazione file e dal terminale riproduzione file.</span><span class="sxs-lookup"><span data-stu-id="25207-104">Two types of track terminals are defined: Recording Track Terminal and Playback Track Terminal, which, respectively, belong to and are managed by File Recording Terminal and File Playback Terminal.</span></span>

<span data-ttu-id="25207-105">Tutti i terminali di rilevamento espongono le interfacce [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) e [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="25207-105">All track terminals expose the [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) and [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interfaces.</span></span> <span data-ttu-id="25207-106">L'interfaccia **ITTerminal** consente la selezione dei terminali di rilevamento nei flussi o nelle chiamate.</span><span class="sxs-lookup"><span data-stu-id="25207-106">The **ITTerminal** interface allows the selection of track terminals onto streams or calls.</span></span>

> [!Note]  
> <span data-ttu-id="25207-107">I terminali di rilevamento espongono anche un'interfaccia privata, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), che viene usata dal msp.</span><span class="sxs-lookup"><span data-stu-id="25207-107">Track terminals also expose a private interface, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), which the MSP uses.</span></span> <span data-ttu-id="25207-108">Le applicazioni non devono tentare di accedere a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="25207-108">Applications should not attempt to access this interface.</span></span>

 

 

 
