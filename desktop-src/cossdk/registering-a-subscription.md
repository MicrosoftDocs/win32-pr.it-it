---
description: Dopo aver registrato una classe di evento nel catalogo COM+, è possibile aggiungere sottoscrittori alla classe di evento e sottoscrizioni ai sottoscrittori.
ms.assetid: 101b1075-3724-4508-9c9e-2f12ac6ab65d
title: Registrazione di una sottoscrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f152834c805bd905019d2afe0e353c0a962452c32ef144cc3c3d445b59fbbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547111"
---
# <a name="registering-a-subscription"></a>Registrazione di una sottoscrizione

Dopo aver registrato una classe di evento nel catalogo COM+, è possibile aggiungere sottoscrittori alla classe di evento e sottoscrizioni ai sottoscrittori. Le sottoscrizioni possono sottoscrivere un singolo metodo o tutti i metodi di un'interfaccia. Per ricevere chiamate su più metodi, ma non su ogni metodo, di un'interfaccia, è necessario aggiungere una sottoscrizione per ogni metodo a cui si vuole ricevere una chiamata. Lo strumento di amministrazione di Servizi componenti può cercare nel catalogo COM+ classi di eventi registrate che supportano le interfacce implementate dal sottoscrittore e offrono la possibilità di effettuare la sottoscrizione. Scegliere l'editore che offre gli eventi desiderati.

Per aggiungere sottoscrittori al componente sottoscrittore, seguire questa procedura:

1.  Dopo aver creato una nuova applicazione COM+ e aver installato il componente sottoscrittore, fare clic con il pulsante destro del mouse sulla cartella **Sottoscrizioni** per abilitare la Creazione guidata nuova sottoscrizione COM+.

2.  Scegliere la classe di evento da cui si vogliono ricevere gli eventi.

3.  Immettere un nome per la sottoscrizione.

4.  Abilitare la sottoscrizione.

5.  Fare clic su **OK**.

Quando un'applicazione di pubblicazione vuole creare un evento, l'editore crea un'istanza dell'oggetto della classe di evento e chiama un metodo su di esso. COM+ cerca nel catalogo COM+ tutti i sottoscrittori. Crea l'oggetto sottoscrittore (direttamente, in coda o con un moniker) e passa la chiamata al metodo originariamente effettuata dal server di pubblicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una classe di evento](registering-an-event-class.md)
</dt> </dl>

 

 



