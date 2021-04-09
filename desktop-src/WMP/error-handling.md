---
title: Gestione degli errori (Windows Media Player SDK)
description: Gestione degli errori
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, gestione degli errori
- Modello a oggetti di Windows Media Player, gestione degli errori
- modello a oggetti, gestione degli errori
- Controllo ActiveX di Windows Media Player, gestione degli errori
- Controllo ActiveX, gestione degli errori
- Controllo ActiveX Windows Media Player Mobile, gestione degli errori
- Windows Media Player Mobile, gestione degli errori
- Guida alla migrazione, gestione degli errori
- gestione degli errori nel modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118731"
---
# <a name="error-handling-windows-media-player-sdk"></a>Gestione degli errori (Windows Media Player SDK)

Il controllo ActiveX Windows Media Player 6,4 fornisce la gestione degli errori predefinita visualizzando i messaggi di errore nelle finestre di dialogo e sulla barra di stato. È anche possibile fornire una gestione degli errori personalizzata elaborando gli errori nello script. La gestione degli errori è basata sugli eventi, ovvero si riceve una notifica per ogni errore e si deve decidere come gestire ogni evento di errore quando si verifica. Per ulteriori informazioni sulla gestione degli errori utilizzando il modello a oggetti della versione 6,4, vedere la sezione relativa alla gestione degli errori della guida del modello a oggetti di versione 6,4, che fa parte di Windows Media Player SDK.

Il modello a oggetti di Windows Media Player 7 o versione successiva fornisce l'oggetto **errore** e l'oggetto **ErrorItem** per la gestione degli errori. Questi due oggetti interagiscono per fornire un meccanismo di gestione degli errori che offre un controllo completo e flessibile del processo di gestione degli errori. L'oggetto **Error** fornisce l'accesso a una raccolta di oggetti **ErrorItem** . ogni oggetto **ErrorItem** fornisce informazioni dettagliate su un singolo messaggio di errore.

Quando si verifica un errore, le informazioni sull'errore vengono inserite in una coda degli errori. La coda è una raccolta di oggetti **ErrorItem** . Poiché ogni errore viene aggiunto alla coda, è associato a un numero di indice (a partire da zero) che può essere usato per identificare l'oggetto **ErrorItem** specifico. *Errore*. la proprietà **ErrorCount** Recupera il numero di errori nella coda degli errori. Poiché i numeri degli indici sono in base zero, l'errore più recente inserito nella coda avrà sempre un valore di indice uguale a *Error*. **ErrorCount** meno uno.

È possibile creare un gestore eventi di errore per Windows Media Player tramite script. Nell'esempio JScript seguente viene illustrato come recuperare l'elemento di errore più recente dalla coda degli errori e visualizzare il codice di errore e la descrizione dell'errore utilizzando il modello a oggetti di Windows Media Player 7 o versione successiva. L'oggetto **Player** è stato creato con ID = "WMP9".


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



L'oggetto **Error** dispone di due metodi aggiuntivi che è possibile utilizzare. *Errore*. il metodo **clearErrorQueue** consente di rimuovere tutti gli errori dalla coda degli errori e di reimpostare il numero di indice su zero. Si dispone del controllo completo su questo processo; è possibile tenere gli errori nella coda per tutto il tempo necessario per renderli disponibili e quindi svuotare la coda al termine della gestione degli errori.

*Errore*. il metodo **WebHelp** consente di visualizzare all'utente le informazioni più aggiornate sull'errore tramite Internet. Quando viene chiamato, questo metodo trasferisce tutte le informazioni rilevanti sul primo errore nella coda (quella con indice zero) a Microsoft Windows Media Player Guida Web, che consente di visualizzare ulteriori informazioni sull'errore nella finestra del browser corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 




