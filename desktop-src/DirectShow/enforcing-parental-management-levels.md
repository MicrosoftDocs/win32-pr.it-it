---
description: Applicazione dei livelli di gestione padre
ms.assetid: ad996a03-e94e-4743-90a2-aa390984a231
title: Applicazione dei livelli di gestione padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7548721613c36369aaa34e5b5a62b665100e9495
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482349"
---
# <a name="enforcing-parental-management-levels"></a>Applicazione dei livelli di gestione padre

Qualsiasi titolo o parte di un titolo in un disco DVD-Video può essere assegnato a un livello di gestione padre (PML) generico da 1 a 8. Quando il navigatore DVD legge contenuto con PML, viene definito in un *blocco padre*. Un blocco parentale può essere costituito da una parte di un capitolo, più capitoli o più titoli. Un'applicazione DVD destinata a un mercato internazionale non dovrebbe codificare in modo rigido un particolare sistema di classificazione nella logica di gestione padre.

Il navigatore DVD non impone il PMLs; informa semplicemente l'applicazione quando rileva le informazioni PML sul disco. Per impostazione predefinita, ignora queste informazioni sul disco e riproduce il contenuto di livello più alto. Per applicare il PMLs, l'applicazione deve implementare una qualche forma di logica di controllo delle password che associ gli utenti ai livelli, indicare allo strumento di spostamento DVD di inviare le notifiche degli eventi PML (chiamando il metodo [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) all'avvio, con i parametri DVD \_ NotifyParentalLevelChange e **true**) e rispondere a tali eventi per consentire o impedire l'accesso in base alle esigenze.

Un titolo DVD può avere un PML generale, ma gli autori di dischi possono assegnare a determinate sezioni del titolo un PMLs più o meno restrittivo. Questi sono denominati comandi PML temporanei; questi comandi contengono sempre due istruzioni di branching: una da seguire se il comando PML temporaneo viene accettato dall'applicazione Player e l'altro da seguire se il comando viene rifiutato. Di seguito è riportata la sequenza di eventi. Il navigatore DVD sta leggendo contenuto video (dominio del titolo DVD) quando rileva un comando PML temporaneo sul disco. Verifica il flag interno per verificare se l'applicazione ha richiesto la notifica di questo evento. Se il flag non è impostato, il DVD continua a essere riprodotto, a seguito del ramo "modifica del livello padre rifiutato" specificato sul disco. Se il flag è impostato, il DVD invia un \_ \_ \_ evento di modifica a livello padre del DVD EC \_ all'applicazione e attende in uno stato di sospensione fino a quando non riceve una risposta. Quando l'applicazione riceve l'evento, usa la propria logica per determinare se accettare il comando. Chiama quindi [**IDVDControl2:: AcceptParentalLevelChange**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-acceptparentallevelchange) con un argomento **true** o **false**. Se il valore è **true**, il navigatore DVD riprende la riproduzione, dopo il ramo "Parental Level Change accepted" specificato sul disco. In caso contrario, riprende la riproduzione e segue il ramo "modifica del livello padre rifiutato".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



