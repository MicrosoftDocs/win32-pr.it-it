---
description: Quando l'utente inizia Visualizzatore eventi per visualizzare le voci del registro eventi, chiama la funzione ReadEventLog per ottenere le strutture EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Visualizzazione del registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227063"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="c668a-103">Visualizzazione del registro eventi</span><span class="sxs-lookup"><span data-stu-id="c668a-103">Viewing the Event Log</span></span>

<span data-ttu-id="c668a-104">Quando l'utente inizia Visualizzatore eventi per visualizzare le voci del registro eventi, chiama la funzione [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) per ottenere le strutture [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="c668a-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="c668a-105">Il Visualizzatore eventi utilizza l'origine evento e l'identificatore evento per ottenere il testo del messaggio per ogni evento dal file di messaggio registrato (indicato dal valore del registro di sistema **EventMessageFile** per l'origine).</span><span class="sxs-lookup"><span data-stu-id="c668a-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="c668a-106">Il Visualizzatore eventi utilizza la funzione [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) per caricare il file di messaggio.</span><span class="sxs-lookup"><span data-stu-id="c668a-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="c668a-107">Il Visualizzatore eventi usa quindi la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) per recuperare la stringa di descrizione di base dal modulo caricato.</span><span class="sxs-lookup"><span data-stu-id="c668a-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="c668a-108">Infine, il Visualizzatore eventi sostituisce i parametri di inserimento nella stringa della descrizione di base per restituire la stringa del messaggio finale.</span><span class="sxs-lookup"><span data-stu-id="c668a-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 
