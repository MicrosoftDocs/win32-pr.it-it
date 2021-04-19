---
description: Segnalazione attività dei controlli padre
ms.assetid: 5ffac4f8-7112-4383-bf73-16e2289a3942
title: Segnalazione attività dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a41527e166b683e2ae7cd72129d9c9f3e032c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315000"
---
# <a name="parental-controls-activity-reporting"></a><span data-ttu-id="35208-103">Segnalazione attività dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="35208-103">Parental Controls Activity Reporting</span></span>

<span data-ttu-id="35208-104">La creazione di report delle attività è considerata fondamentale in base ai problemi di ingegneria sociale.</span><span class="sxs-lookup"><span data-stu-id="35208-104">Activity reporting is considered essential given social engineering issues.</span></span> <span data-ttu-id="35208-105">Le applicazioni o i filtri in grado di riconoscere le attività vengono richieste come specificato nella sezione Utilizzo delle API dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="35208-105">Aware applications or filters are requested to log activities as specified in the Using Parental Controls APIs section.</span></span>

<span data-ttu-id="35208-106">Facendo clic sul collegamento report attività viene visualizzata una pagina di Log Viewer che Mostra tutte le voci di log per un intervallo massimo di una settimana, delimitato in base ai limiti della dimensione del log, con i riquadri dati in formato colonna e albero categoria.</span><span class="sxs-lookup"><span data-stu-id="35208-106">Clicking the Activity reporting link brings up a Log Viewer page showing all log entries for a maximum one week interval (further bounded by log size limits), with category tree and column format data panes.</span></span>

<span data-ttu-id="35208-107">Nella casella riepilogo nella parte superiore destra del pannello controlli padre è indicato lo stato corrente per la creazione di report delle attività.</span><span class="sxs-lookup"><span data-stu-id="35208-107">The summary box in the upper right of the Parental Controls Panel indicates current status for activity reporting.</span></span>

<span data-ttu-id="35208-108">Gli eventi di attività sono visibili anche nel Visualizzatore eventi con il nome Microsoft.com/Windows/ParentalControls nei log dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35208-108">Activity events are also visible in the Event Viewer with a name of Microsoft.com/Windows/ParentalControls in the Application Logs.</span></span>

<span data-ttu-id="35208-109">Questa funzionalità dipende dalle nuove funzionalità di registrazione eventi in Windows Vista, usando le API di pubblicazione fornite.</span><span class="sxs-lookup"><span data-stu-id="35208-109">This functionality depends on the new Event Logging functionality in Windows Vista, using the provided Publishing APIs.</span></span>

 

 



