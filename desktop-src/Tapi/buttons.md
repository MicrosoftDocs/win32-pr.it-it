---
description: La telefonia Microsoft modella i pulsanti e le lampade del telefono come coppie pulsante-lampada.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Pulsanti (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309974"
---
# <a name="buttons-telephony-api"></a>Pulsanti (API di telefonia)

La telefonia Microsoft modella i pulsanti e le lampade di un telefono come coppie di pulsanti. Un pulsante senza lampada accanto o una lampada senza pulsante viene specificato usando un indicatore fittizio per la lampada o il pulsante mancante. Un pulsante con più lampade viene modellato usando più coppie di pulsanti.

È possibile impostare e recuperare le informazioni associate a un pulsante del telefono. Quando si preme un pulsante, il provider di servizi invia un messaggio di un [**\_ pulsante telefonico**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) alla funzione di callback TAPI. I parametri di questo messaggio sono un handle per il dispositivo telefonico e l'identificatore pulsante/lampada del pulsante premuto. Al pulsante del tastierino da' 0' a' 9',' \* ' è \# ' vengono assegnati gli identificatori di pulsante/lampo fissi da 0 a 11.

La funzione [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) imposta le informazioni associate a un pulsante in un dispositivo telefonico. [**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) restituisce le informazioni associate a un pulsante in un dispositivo telefonico. Il provider di servizi invia un \_ messaggio di pulsante telefonico alla funzione di callback TAPI quando viene premuto un pulsante sul telefono.

Le informazioni associate a un pulsante non contengono alcun significato semantico per quanto concerne TSPI. È utile per le applicazioni specifiche del dispositivo che interpretano queste informazioni per un determinato dispositivo telefonico o per la visualizzazione all'utente, ad esempio nel sistema della Guida di un'applicazione.

 

 
