---
description: I terminali dei file possono essere utilizzati in due modi.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Uso di terminali file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131926"
---
# <a name="using-file-terminals"></a><span data-ttu-id="eff73-103">Uso di terminali file</span><span class="sxs-lookup"><span data-stu-id="eff73-103">Using File Terminals</span></span>

<span data-ttu-id="eff73-104">I terminali dei file possono essere utilizzati in due modi.</span><span class="sxs-lookup"><span data-stu-id="eff73-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="eff73-105">Il metodo più semplice consiste nell'usare [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) per selezionare un file Terminal (riproduzione o record) su un oggetto chiamata TAPI.</span><span class="sxs-lookup"><span data-stu-id="eff73-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="eff73-106">In questo caso TAPI si occupa della connessione dei flussi audio ai terminali di tracking.</span><span class="sxs-lookup"><span data-stu-id="eff73-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="eff73-107">Il secondo metodo consente a un'applicazione di avere un controllo più preciso sul mapping dei flussi audio alle tracce.</span><span class="sxs-lookup"><span data-stu-id="eff73-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="eff73-108">In questo scenario, l'applicazione enumera i flussi disponibili nella chiamata, seleziona quelli che vuole registrare (o usare per la riproduzione), crea (o trova per la riproduzione) le tracce corrispondenti nel terminale file e seleziona le tracce nei flussi di chiamata.</span><span class="sxs-lookup"><span data-stu-id="eff73-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="eff73-109">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="eff73-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="eff73-110">Riproduzione semplice</span><span class="sxs-lookup"><span data-stu-id="eff73-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="eff73-111">Riproduzione controllata dal rilevamento</span><span class="sxs-lookup"><span data-stu-id="eff73-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="eff73-112">Record semplice</span><span class="sxs-lookup"><span data-stu-id="eff73-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="eff73-113">Record controllato dal rilevamento</span><span class="sxs-lookup"><span data-stu-id="eff73-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



