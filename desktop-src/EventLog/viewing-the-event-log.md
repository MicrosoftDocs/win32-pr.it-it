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
# <a name="viewing-the-event-log"></a>Visualizzazione del registro eventi

Quando l'utente inizia Visualizzatore eventi per visualizzare le voci del registro eventi, chiama la funzione [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) per ottenere le strutture [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . Il Visualizzatore eventi utilizza l'origine evento e l'identificatore evento per ottenere il testo del messaggio per ogni evento dal file di messaggio registrato (indicato dal valore del registro di sistema **EventMessageFile** per l'origine). Il Visualizzatore eventi utilizza la funzione [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) per caricare il file di messaggio. Il Visualizzatore eventi usa quindi la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) per recuperare la stringa di descrizione di base dal modulo caricato. Infine, il Visualizzatore eventi sostituisce i parametri di inserimento nella stringa della descrizione di base per restituire la stringa del messaggio finale.

 

 
