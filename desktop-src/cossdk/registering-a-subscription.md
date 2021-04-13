---
description: Dopo la registrazione di una classe di evento nel catalogo COM+, è possibile aggiungere sottoscrittori alla classe di evento e alle sottoscrizioni dei sottoscrittori.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrazione di una sottoscrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03d5710fc792cad6282683d51df21d2ede10451
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401486"
---
# <a name="registering-a-subscription"></a>Registrazione di una sottoscrizione

Dopo la registrazione di una classe di evento nel catalogo COM+, è possibile aggiungere sottoscrittori alla classe di evento e alle sottoscrizioni dei sottoscrittori. Le sottoscrizioni possono sottoscrivere un solo metodo o tutti i metodi di un'interfaccia. Per ricevere chiamate su più di un metodo, ma non su ogni metodo, di un'interfaccia, è necessario aggiungere una sottoscrizione per ogni metodo a cui si desidera ricevere una chiamata. Lo strumento di amministrazione Servizi componenti può eseguire ricerche nel catalogo COM+ per le classi di evento registrate che supportano le interfacce implementate dal Sottoscrittore e offre la possibilità di effettuare la sottoscrizione. Scegliere il server di pubblicazione che offre gli eventi desiderati.

Per aggiungere i Sottoscrittori al componente del Sottoscrittore, attenersi alla procedura seguente:

1.  Dopo aver creato una nuova applicazione COM+ e installato il componente del Sottoscrittore, fare clic con il pulsante destro del mouse sulla cartella **sottoscrizioni** per abilitare la creazione guidata nuova sottoscrizione com+.

2.  Scegliere la classe di evento da cui si desidera ricevere gli eventi.

3.  Immettere un nome per la sottoscrizione.

4.  Abilitare la sottoscrizione.

5.  Fare clic su **OK**.

Quando un'applicazione del server di pubblicazione desidera generare un evento, il server di pubblicazione crea un'istanza dell'oggetto classe di evento e chiama un metodo su di esso. COM+ esegue una ricerca nel catalogo COM+ per trovare tutti i sottoscrittori. Crea l'oggetto sottoscrittore (direttamente, in coda o con un moniker) e passa la chiamata al metodo originariamente eseguita dal server di pubblicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una classe di evento](registering-an-event-class.md)
</dt> </dl>

 

 



