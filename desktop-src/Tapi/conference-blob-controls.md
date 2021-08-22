---
description: Il diagramma seguente illustra gli oggetti principali coinvolti nei controlli BLOB per conferenze TAPI 3. Le interfacce visualizzate sono con collegamenti ipertestuali nelle pagine di riferimento pertinenti.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Conference Blob Controls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1361951fcb830676e36acb4ec397832629dc5745983c654317a457a0d66ac336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867994"
---
# <a name="conference-blob-controls"></a>Conference Blob Controls

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il diagramma seguente illustra gli oggetti principali coinvolti nei controlli BLOB per conferenze TAPI 3. Le interfacce visualizzate sono con collegamenti ipertestuali nelle pagine di riferimento pertinenti.

![interfacce e controlli BLOB per conferenze](images/rendblob.png)

Il BLOB della conferenza contiene informazioni specifiche del provider su un oggetto conferenza. Un puntatore al BLOB [**dell'interfaccia ITConferenceBlob**](itconferenceblob.md) viene ottenuto eseguendo queryInterface su [**ITDirectoryObjectConference.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) **L'interfaccia ITConferenceBlob fornisce** metodi per la manipolazione di base di un BLOB di conferenze generico. Un'applicazione che usa BLOB di conferenze non SDP deve implementare i propri metodi per la manipolazione dei dettagli.

Rendezvous fornisce [**l'interfaccia ITSdp**](itsdp.md) per la modifica dei BLOB di conferenze SDP. SDP è un protocollo per la descrizione delle sessioni multimediali e delle relative informazioni di pianificazione. Per altre informazioni sul protocollo SDP, individuare Internet Engineering Task Force (IETF) RFC 2327 intitolato "SDP: Session Description Protocol". Se **l'interfaccia ITSDP** esiste per un blob di conferenze specificato, è possibile ottenere un puntatore eseguendo **queryInterface** su [**ITConferenceBlob.**](itconferenceblob.md)

Per i BLOB di conferenze SDP, le interfacce [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)e [**ITMedia**](itmedia.md) consentono un controllo dettagliato del tempo di conferenza SDP e delle caratteristiche multimediali.

 

 



