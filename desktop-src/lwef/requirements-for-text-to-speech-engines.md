---
title: Requisiti per i motori di sintesi vocale
description: Requisiti per i motori di sintesi vocale
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471342"
---
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="75709-103">Requisiti per i motori di sintesi vocale</span><span class="sxs-lookup"><span data-stu-id="75709-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="75709-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="75709-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="75709-105">Il motore deve essere completamente compatibile con SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="75709-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="75709-106">Inoltre, il motore deve supportare anche le interfacce SAPI seguenti per le notifiche di testo e segnalibro con tag.</span><span class="sxs-lookup"><span data-stu-id="75709-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="75709-107">Queste interfacce consentono a Microsoft Agent di eseguire il ritmo dell'output del testo in un fumetto di parole di un carattere e di sincronizzare il labbro della bocca (o equivalente) del carattere con le parole pronunciate.</span><span class="sxs-lookup"><span data-stu-id="75709-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="75709-108">ITTSCentralW</span><span class="sxs-lookup"><span data-stu-id="75709-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="75709-109">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="75709-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="75709-110">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="75709-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="75709-111">ITTSAttributesW</span><span class="sxs-lookup"><span data-stu-id="75709-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




