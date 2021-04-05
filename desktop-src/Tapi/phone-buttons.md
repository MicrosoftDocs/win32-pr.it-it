---
description: TAPI modella i pulsanti e le lampade del telefono come coppie pulsante-lampada.
ms.assetid: e4c50bd6-a256-407f-af3b-b24383a30ea0
title: Pulsanti telefono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e65c34096c0cf043b85d80c9c726c6bef982d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755111"
---
# <a name="phone-buttons"></a>Pulsanti telefono

TAPI modella i pulsanti e le lampade di un telefono come coppie pulsante-lampada. Un pulsante senza lampada accanto o una lampada senza pulsante viene specificato usando un indicatore "fittizio" per la lampada o il pulsante mancante. Un pulsante con più lampade viene modellato usando più coppie di pulsanti.

È possibile impostare e recuperare le informazioni associate a un pulsante del telefono. Quando si preme un pulsante, alla funzione dell'applicazione viene inviato un messaggio di un [**\_ pulsante telefonico**](phone-button.md) . I parametri di questo messaggio sono un handle per il dispositivo telefonico e l'identificatore della lampada pulsante del pulsante premuto. Ai pulsanti di tastiera da' 0' a' 9',' \* ' è \# ' vengono assegnati gli identificatori di pulsanti fissi da 0 a 11.

Le funzioni associate ai pulsanti sono [**phoneSetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo), che consente di impostare le informazioni associate a un pulsante in un dispositivo telefonico e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo), che restituisce informazioni associate a un pulsante in un dispositivo telefonico. Il \_ messaggio del pulsante telefonico viene inviato a un'applicazione quando viene premuto un pulsante sul telefono.

Le informazioni associate a un pulsante non contengono alcun significato semantico per quanto riguarda TAPI. È utile per le applicazioni specifiche del dispositivo che comprendono il significato di queste informazioni per un determinato dispositivo telefonico o per la visualizzazione all'utente, ad esempio la Guida in linea.

 

 



