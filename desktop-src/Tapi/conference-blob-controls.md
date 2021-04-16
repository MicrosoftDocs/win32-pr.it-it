---
description: Il diagramma seguente illustra gli oggetti principali inclusi nei controlli BLOB della conferenza TAPI 3. Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controlli BLOB conferenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527223"
---
# <a name="conference-blob-controls"></a>Controlli BLOB conferenza

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il diagramma seguente illustra gli oggetti principali inclusi nei controlli BLOB della conferenza TAPI 3. Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.

![interfacce e controlli BLOB della conferenza](images/rendblob.png)

Il BLOB della conferenza contiene informazioni specifiche del provider su un oggetto Conference. Un puntatore al BLOB dell'interfaccia [**ITConferenceBlob**](itconferenceblob.md) viene ottenuto eseguendo un QueryInterface in [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference). L'interfaccia **ITConferenceBlob** fornisce metodi per la manipolazione di base di un BLOB di conferenze generiche. Un'applicazione che usa BLOB di conferenze non SDP deve implementare i propri metodi per la manipolazione dei dettagli.

Rendezvous fornisce l'interfaccia [**ITSdp**](itsdp.md) per la manipolazione dei BLOB delle conferenze SDP. SDP è un protocollo per la descrizione delle sessioni multimediali e delle relative informazioni di pianificazione. Per ulteriori informazioni sul protocollo SDP, individuare Internet Engineering Task Force (IETF) RFC 2327 denominato "SDP: Session Description Protocol". Se l'interfaccia **ITSDP** esiste per un BLOB di conferenza specifico, è possibile ottenere un puntatore a tale BLOB eseguendo un **QueryInterface** in [**ITConferenceBlob**](itconferenceblob.md).

Per i BLOB di conferenze SDP, le interfacce [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)e [**ITmedia**](itmedia.md) consentono un controllo dettagliato delle caratteristiche dei supporti e dei tempi delle conferenze SDP.

 

 



