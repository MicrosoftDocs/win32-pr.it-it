---
description: L'operazione di parcheggio consente a un'applicazione di inviare una sessione a un indirizzo speciale in cui verrà mantenuta fino a quando non viene parcheggiato.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Park
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312714"
---
# <a name="park"></a>Park

L'operazione di parcheggio consente a un'applicazione di inviare una sessione a un indirizzo speciale in cui verrà mantenuta fino a quando non viene parcheggiato. Dal punto di vista dell'applicazione, questo aspetto è molto simile a quello di un trasferimento. All'entità nell'altra estremità della connessione, questo aspetto è simile a quello in attesa.

La differenza tra Park e transfer consiste nel fatto che l'indirizzo parcheggiato non è un punto di connessione per la sessione e la sessione non avverte alcun timeout. La differenza tra Park e Holding è che una volta completata l'operazione di Park, la sessione non è più associata all'indirizzo dell'applicazione.

Sono disponibili due forme di parcheggio per una sessione: *Park diretto* e non *diretto*. In directed Call Park, l'applicazione specifica l'indirizzo di destinazione in cui deve essere parcheggiata la chiamata. Con un parcheggio non diretto, il provider di servizi o l'hardware sottostante determina l'indirizzo e lo restituisce all'applicazione.

Una sessione parcheggiata in genere entra nello stato inattivo dopo che è stata parcheggiata correttamente e l'applicazione deve quindi rilasciare le risorse associate. Per un riepilogo su come eseguire questa operazione, vedere [terminare una sessione](terminate-a-session-ovr.md) .

Se l'applicazione Sblocca la sessione, vengono allocate nuove risorse della sessione anche se l'applicazione ha restituito i puntatori precedenti, pertanto l'esito negativo delle versioni appropriate può causare diversi problemi.

Alcuni provider di servizi possono ricordare all'utente che una sessione è stata parcheggiata per un lungo periodo di tempo. L'applicazione visualizza una chiamata a un'offerta con un [motivo](reason-ovr.md) della chiamata impostato su promemoria.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).

**TAPI 3:** Vedere [**ITBasicCallControl::P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).

 

 
