---
description: TAPI modella i pulsanti e le lampadine dei telefoni come coppie pulsante-lampione.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Telefono Pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e72288133615b19e622434b8727608aaec9a9136dd58eaa03e339708c42a13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774161"
---
# <a name="phone-buttons"></a>Telefono Pulsanti

TAPI modella i pulsanti e le lampadine di un telefono come coppie pulsante-lampione. Un pulsante senza lampadina accanto o una lampadina senza pulsante viene specificato usando un indicatore "fittizio" per la lampadina o il pulsante mancante. Un pulsante con più lampadine viene modellato usando più coppie di pulsanti-lampe.

Le informazioni associate a un pulsante telefono possono essere impostate e recuperate. Quando si preme un pulsante, viene inviato un [**messaggio \_ PHONE BUTTON**](phone-button.md) alla funzione dell'applicazione. I parametri di questo messaggio sono un handle per il dispositivo telefonico e l'identificatore della lampadina del pulsante che è stato premuto. Ai pulsanti del tastierino numerico da '0' a '9', '' e '' vengono assegnati gli identificatori fissi della lampadina dei pulsanti da 0 a \* \# 11.

Le funzioni associate ai pulsanti sono [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), che imposta le informazioni associate a un pulsante in un dispositivo telefono, e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), che restituisce informazioni associate a un pulsante in un dispositivo telefono. Il messaggio \_ PHONE BUTTON viene inviato a un'applicazione quando viene premuto un pulsante sul telefono.

Le informazioni associate a un pulsante non hanno alcun significato semantico per quanto riguarda TAPI. È utile per le applicazioni specifiche del dispositivo che comprendono il significato di queste informazioni per un determinato dispositivo telefonico o per la visualizzazione all'utente, ad esempio la Guida online.

 

 



