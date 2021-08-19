---
description: Applicazione dei livelli di gestione dei genitori
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Applicazione dei livelli di gestione dei genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58bb9613af2bafb353df15bd84849724890faeb5c1191701cf2599522fd26fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819934"
---
# <a name="enforcing-parental-management-levels"></a>Applicazione dei livelli di gestione dei genitori

A qualsiasi titolo o parte di un titolo DVD-Video disco può essere assegnato un livello PML (Parental Management Level) generico da 1 a 8. Quando lo strumento di navigazione DVD legge contenuto con un file PML, si dice che si trova in un *blocco di genitori.* Un blocco di genitori può essere costituito da parte di un capitolo, più capitoli o più titoli. Un'applicazione DVD destinata a un mercato internazionale non deve codificare un particolare sistema di classificazione nella logica di gestione dei genitori.

Lo strumento di navigazione DVD non applica le pml. si limita a informare l'applicazione quando rileva informazioni PML sul disco. Per impostazione predefinita, ignora queste informazioni sul disco e riproduce il contenuto di livello più alto. Per applicare le regole PML, l'applicazione deve implementare una forma di logica di controllo delle password che associa gli utenti ai livelli, indicare al dvd navigator di inviare notifiche degli eventi PML (chiamando il metodo [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) all'avvio, con i parametri DVD \_ NotifyParentalLevelChange e **TRUE)** e rispondere a tali eventi per consentire o non consentire l'accesso in base alle esigenze.

Un titolo DVD può avere un file PML complessivo, ma gli autori di dischi possono assegnare determinate sezioni di tale titolo a file PML più alti o più restrittivi. Questi comandi sono detti comandi PML temporanei. questi comandi contengono sempre due istruzioni di diramazione: una da seguire se il comando PML temporaneo viene accettato dall'applicazione lettore e l'altro da seguire se il comando viene rifiutato. La sequenza di eventi è la seguente. Lo strumento di navigazione DVD legge il contenuto video (DVD Title Domain) quando rileva un comando PML temporaneo sul disco. Controlla il flag interno per verificare se l'applicazione ha richiesto di ricevere una notifica di questo evento. Se il flag non è impostato, la riproduzione del DVD continua a seguire il ramo "parent level change rejected" specificato sul disco. Se il flag è impostato, il DVD invia un evento EC DVD PARENTAL LEVEL CHANGE all'applicazione e attende in stato di sospensione fino a quando non \_ \_ ottiene una \_ \_ risposta. Quando l'applicazione riceve l'evento, usa la propria logica per determinare se accettare il comando. Chiama quindi [**IDvdControl2::AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) con un argomento **TRUE** o **FALSE.** Se **TRUE,** lo strumento di navigazione DVD riprende la riproduzione, seguendo il ramo "parent level change accepted" specificato sul disco. In caso contrario, riprende la riproduzione e segue il ramo "modifica del livello genitoriale rifiutata".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



