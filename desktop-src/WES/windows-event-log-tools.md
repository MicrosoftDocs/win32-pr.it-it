---
title: Strumenti del registro eventi di Windows
description: Nel registro eventi di Windows sono disponibili gli strumenti seguenti per la compilazione del provider.
ms.assetid: 20087fdf-3e9f-4090-8103-5864f1c9753c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e604c291ff1046789ef9f3efba00ebb7305122
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104398803"
---
# <a name="windows-event-log-tools"></a><span data-ttu-id="801a2-103">Strumenti del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="801a2-103">Windows Event Log Tools</span></span>

<span data-ttu-id="801a2-104">Nel registro eventi di Windows sono disponibili gli strumenti seguenti per la compilazione del provider.</span><span class="sxs-lookup"><span data-stu-id="801a2-104">Windows Event Log provides the following tools that you use to build your provider.</span></span>



| <span data-ttu-id="801a2-105">Strumento</span><span class="sxs-lookup"><span data-stu-id="801a2-105">Tool</span></span>                                                           | <span data-ttu-id="801a2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="801a2-106">Description</span></span>                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="801a2-107">**Compilatore di messaggi (MC.exe)**</span><span class="sxs-lookup"><span data-stu-id="801a2-107">**Message Compiler (MC.exe)**</span></span>](message-compiler--mc-exe-.md)  | <span data-ttu-id="801a2-108">Utilità della riga di comando utilizzata per compilare manifesti di strumentazione e file di testo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="801a2-108">A command line utility used to compile instrumentation manifests and message text files.</span></span> |
| <span data-ttu-id="801a2-109">WevtUtil.exe</span><span class="sxs-lookup"><span data-stu-id="801a2-109">WevtUtil.exe</span></span>                                                   | <span data-ttu-id="801a2-110">Utilità della riga di comando utilizzata principalmente per registrare il provider nel computer.</span><span class="sxs-lookup"><span data-stu-id="801a2-110">A command line utility used primarily to register your provider on the computer.</span></span> <span data-ttu-id="801a2-111">È inoltre possibile utilizzarlo per ottenere informazioni sui metadati sul provider, i relativi eventi e i canali in cui vengono registrati gli eventi e per eseguire query sugli eventi da un canale o un file di log.</span><span class="sxs-lookup"><span data-stu-id="801a2-111">You can also use it to get metadata information about the provider, its events, and the channels to which it logs events, and to query events from a channel or log file.</span></span> <span data-ttu-id="801a2-112">Lo strumento WevtUtil.exe è incluso in% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="801a2-112">The WevtUtil.exe tool is included in %windir%\\System32.</span></span> <span data-ttu-id="801a2-113">Per informazioni sull'utilizzo, immettere "wevtutil/?"</span><span class="sxs-lookup"><span data-stu-id="801a2-113">For usage information, enter "wevtutil /?"</span></span> <span data-ttu-id="801a2-114">al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="801a2-114">at a command prompt.</span></span><br/> <span data-ttu-id="801a2-115">Questo comando è limitato ai membri del gruppo Administrators e deve essere eseguito con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="801a2-115">This command is limited to members of the Administrators group and must be run with elevated privileges.</span></span>|
