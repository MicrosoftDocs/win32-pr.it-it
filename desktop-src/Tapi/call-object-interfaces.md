---
description: L'oggetto chiamata viene creato quando entra in vigore una chiamata. Le interfacce associate ottengono e impostano informazioni relative alla chiamata.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Chiama interfacce oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967602"
---
# <a name="call-object-interfaces"></a>Chiama interfacce oggetto

L' [oggetto chiamata](call-object.md) viene creato quando entra in vigore una chiamata. Le interfacce associate ottengono e impostano informazioni relative alla chiamata.

Le interfacce dell'enumeratore e degli eventi non sono direttamente esposte nell'oggetto chiamata, ma sono elencate qui per praticità di riferimento.

Le interfacce [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent), [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent), [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent), [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)e [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) non sono direttamente esposte sull'oggetto chiamata, ma sono strettamente correlate e sono elencate di seguito per praticità di riferimento.



| Interfaccia                                                      | Descrizione                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Fornisce informazioni relative a un oggetto chiamata, ad esempio lo stato della chiamata o i terminali in uso.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Estende [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) fornendo metodi per impostare il filtraggio degli eventi in base a ogni chiamata.                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Utilizzato per connettersi, rispondere ed eseguire operazioni di base di telefonia su un oggetto chiamata.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Estende [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) fornendo metodi per selezionare un terminale in una chiamata.              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Interfaccia di notifica per [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Interfaccia di notifica per le modifiche nelle informazioni sulle chiamate.                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Ottiene informazioni relative a un evento di chiamata.                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Ottiene informazioni relative a un evento del supporto di chiamata.                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Fornisce metodi per controllare i toni personalizzati possibili con alcuni set di telefono.                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Fornisce metodi per specificare i toni e le caratteristiche dei toni che generano eventi di tono.                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Supporta le applicazioni legacy che devono comunicare direttamente con un dispositivo.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Estende [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) fornendo metodi per il rilevamento e la generazione di un tono. |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Enumera [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



