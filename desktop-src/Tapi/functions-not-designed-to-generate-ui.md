---
description: Si supponga che il provider di servizi debba visualizzare una finestra di dialogo (come la finestra di dialogo UniModel o ATSP Talk/hangup) durante l'elaborazione di lineMakeCall o lineDial.
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: Funzioni non progettate per generare l'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bd7ed1395136d1a2d2a31b060127395e8804ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529065"
---
# <a name="functions-not-designed-to-generate-ui"></a>Funzioni non progettate per generare l'interfaccia utente

Si supponga che il provider di servizi debba visualizzare una finestra di dialogo (come la finestra di dialogo UniModel o ATSP **Talk/hangup** ) durante l'elaborazione di [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) o [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial). In questo caso, è il provider di servizi, non l'applicazione, che decide che l'interfaccia utente deve essere visualizzata.

Per richiamare la DLL dell'interfaccia utente nel processo dell'applicazione, il provider di servizi chiama il callback dell' [*\_ evento della riga*](/windows/win32/api/tspi/nc-tspi-lineevent) TSPI, generando un messaggio di [**\_ CREATEDIALOGINSTANCE di riga**](line-createdialoginstance.md) , passando un puntatore a una struttura di tipo [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams). Questa struttura contiene l' **dwRequestID** della funzione a cui è associata l'interfaccia utente, consentendo a tapisrv di identificare l'applicazione client in cui deve essere generata l'interfaccia utente.

TAPISRV richiede l'istanza dell'applicazione corretta di TAPI per caricare la DLL dell'interfaccia utente e creare un thread per l'interfaccia utente all'interno del processo dell'applicazione. Da questo nuovo thread dell'interfaccia utente, TAPI chiama la funzione [**TUISPI \_ PROVIDERGENERICDIALOG**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) della DLL dell'interfaccia utente, passando i dati specificati dal provider del servizio di telefonia nella struttura passata con il messaggio di [**riga \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) . nella DLL dell'interfaccia utente viene visualizzata la finestra di dialogo appropriata, che è importante per la progettazione privata tra la DLL dell'interfaccia utente e il provider del servizio di telefonia. La DLL dell'interfaccia utente non restituisce da **TUISPI \_ providerGenericDialog** fino a quando la finestra di dialogo non viene chiusa.

Il provider di servizi di telefonia può generare dati aggiornati da visualizzare nella finestra di dialogo (o, ad esempio, indicare la chiusura della finestra di dialogo, se la chiamata viene abbandonata o se si verificano altri eventi) inviando un messaggio [**\_ SENDDIALOGINSTANCEDATA di riga**](line-senddialoginstancedata.md) . TAPISRV trasmette i dati a TAPI, che chiama la funzione [**TUISPI \_ PROVIDERGENERICDIALOGDATA**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) della DLL dell'interfaccia utente. Questo meccanismo fornisce una "trasmissione" unidirezionale alla DLL dell'interfaccia utente. Se la DLL dell'interfaccia utente desidera informare il provider di servizi di telefonia dei risultati della finestra di dialogo o ottenere altri dati, è possibile chiamare la funzione [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) (un puntatore al quale è stato ricevuto quando è stato chiamato [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) ).

Quando la finestra di dialogo viene rilasciata, [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) torna a TAPI. TAPI chiama [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) per rilasciare la DLL dell'interfaccia utente e chiude il thread dell'interfaccia utente creato nel contesto dell'applicazione. Richiede quindi a TAPISRV di chiamare la funzione [**TSPI \_ providerFreeDialogInstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) del provider di servizi di telefonia per annullare l'associazione dell'associazione creata quando il provider del servizio di telefonia ha inviato originariamente il messaggio di [**riga \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md) . Questa funzione viene chiamata anche se il processo dell'applicazione termina in modo imprevisto prima della restituzione di **TUISPI \_ providerGenericDialog** .

 

 
