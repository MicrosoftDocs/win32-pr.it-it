---
title: Controllare Spy v 2.0
description: Control Spy è uno strumento che aiuta gli sviluppatori a comprendere i controlli comuni su come applicare gli stili e come rispondono a messaggi e notifiche.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047528"
---
# <a name="control-spy-v20"></a>Controllare Spy v 2.0

Controllo Spy è uno strumento che consente agli sviluppatori di comprendere i controlli comuni: come applicare gli stili e come rispondono a messaggi e notifiche. Utilizzando Spy Control, è possibile visualizzare immediatamente il modo in cui gli stili diversi influiscono sul comportamento e sull'aspetto di ogni controllo e su come è possibile modificare lo stato di ogni controllo inviando messaggi.

Sono disponibili due versioni di Spy Control, una per [Comctl32.dll versione 5. x](common-control-versions.md) e una per Comctl32.dll versione 6,0 e successive. ControlSpyV6.exe dispone di un manifesto dell'applicazione incorporato in modo che utilizzi i controlli con tema più recenti. ControlSpyV5.exe non dispone di questo manifesto e pertanto il valore predefinito è la versione precedente.

In questo argomento sono contenute le sezioni seguenti.

-   [Overview](#overview)
-   [Stili](#styles)
-   [Messaggi](#messages)
-   [Dimensioni/colore](#sizecolor)
-   [Dove ottenere il controllo Spy](#where-to-get-control-spy)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Il controllo Spy ospita un controllo comune selezionato al centro della finestra dell'applicazione. È possibile modificare il controllo visualizzato selezionando diversi controlli dalla casella di riepilogo sul lato sinistro della finestra. I messaggi o le notifiche ricevute dal controllo verranno elencati sul lato destro della finestra man mano che arrivano. È possibile abilitare o disabilitare questa funzionalità usando le caselle di controllo **messaggi ricevuti** e **notifiche ricevute** .

La figura seguente mostra l'applicazione Control Spy.

![finestra Spy di controllo](images/controlspy-main.png)

Nella parte inferiore della finestra sono disponibili diverse schede in cui sono presenti più funzionalità.

## <a name="styles"></a>Stili

La scheda **stili** consente di modificare lo stile della finestra corrente del controllo. Selezionare o deselezionare uno degli stili elencati, quindi fare clic sul pulsante **applica** per modificare lo stile del controllo visualizzato. In alternativa, è possibile usare il pulsante **ricrea** per creare un nuovo controllo con gli stili selezionati. Il pulsante **Reimposta** restituirà il controllo agli stili predefiniti.

I pulsanti copia **stile** e **copia ExStyle** sotto la scheda copieranno le costanti di stile selezionate negli Appunti come elenco delimitato or bit per bit ( \| ). È possibile incollare questo elenco direttamente nella chiamata a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per fornire un controllo nella propria applicazione con lo stesso stile.

La figura seguente mostra la scheda **stili** per un controllo Button.

![scheda stili spia di controllo](images/controlspy-styles.png)

## <a name="messages"></a>Messaggi

La scheda **messaggi** consente di inviare quasi tutti i messaggi a un controllo. Dopo aver selezionato un messaggio dalla casella di riepilogo, è possibile immettere i dati inviati come parametri *wParam* e *lParam* della chiamata a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage). Dopo aver fatto clic su **Invia**, il messaggio viene inviato al controllo e tutti i risultati vengono visualizzati nella casella di testo nella parte inferiore della scheda.

La figura seguente mostra la scheda messaggi quando viene selezionato un messaggio specifico.

![scheda messaggi di controllo Spy](images/controlspy-messages.png)

## <a name="sizecolor"></a>Dimensioni/colore

La scheda **dimensioni/colore** può essere utilizzata per modificare le dimensioni del controllo e il colore dello sfondo.

## <a name="where-to-get-control-spy"></a>Dove ottenere il controllo Spy

È possibile scaricare il [controllo Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) da MSDN. Entrambe le versioni sono contenute nel download.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Controlli Windows](window-controls.md)
</dt> <dt>

[Abilitazione degli stili di visualizzazione](cookbook-overview.md)
</dt> </dl>

 

 