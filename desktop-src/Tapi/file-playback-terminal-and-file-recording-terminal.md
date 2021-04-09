---
description: Il terminale per la riproduzione di file e il terminale di registrazione file espongono le interfacce ITTerminal e ITMultiTrackTerminal. Questi oggetti espongono anche l'interfaccia ITMediaControl, che fornisce metodi per l'arresto, l'avvio e la navigazione multimediale.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminale di riproduzione file e terminale di registrazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967468"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a><span data-ttu-id="c3cba-104">Terminale di riproduzione file e terminale di registrazione file</span><span class="sxs-lookup"><span data-stu-id="c3cba-104">File Playback Terminal and File Recording Terminal</span></span>

<span data-ttu-id="c3cba-105">Il terminale per la riproduzione di file e il terminale di registrazione file espongono le interfacce [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) e [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) .</span><span class="sxs-lookup"><span data-stu-id="c3cba-105">The File Playback Terminal and File Recording Terminal expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) and [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interfaces.</span></span> <span data-ttu-id="c3cba-106">Questi oggetti espongono anche l'interfaccia [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , che fornisce metodi per l'arresto, l'avvio e la navigazione multimediale.</span><span class="sxs-lookup"><span data-stu-id="c3cba-106">These objects also expose the [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) interface, which provides methods for stopping, starting, and media navigation.</span></span>

<span data-ttu-id="c3cba-107">Il terminale per la riproduzione di file espone l'interfaccia [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , che include metodi specifici per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c3cba-107">The File Playback Terminal exposes the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface, which has playback-specific methods.</span></span>

<span data-ttu-id="c3cba-108">Il terminale di registrazione file espone l'interfaccia [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , che fornisce metodi specifici per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="c3cba-108">The File Recording Terminal exposes the [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) interface, which provides recording-specific methods.</span></span>

<span data-ttu-id="c3cba-109">Come [terminali multitraccia](multitrack-terminals.md), il terminale per la registrazione di file e il terminale di riproduzione file gestiscono una raccolta di [terminali Track](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="c3cba-109">As [multitrack terminals](multitrack-terminals.md), File Recording Terminal and File Playback Terminal each manage a collection of [track terminals](track-terminals.md).</span></span>

 

 
