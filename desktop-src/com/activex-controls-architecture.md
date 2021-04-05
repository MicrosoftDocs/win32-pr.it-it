---
title: Architettura di controlli ActiveX
description: La tecnologia controlli ActiveX si basa su una base di molti oggetti di livello inferiore e interfacce in OLE. Le interfacce esatte disponibili in un controllo variano in base alle relative funzionalità. In questa sezione vengono esaminate in dettaglio le funzionalità che possono essere fornite da un controllo.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709553"
---
# <a name="activex-controls-architecture"></a>Architettura di controlli ActiveX

La tecnologia controlli ActiveX si basa su una base di molti oggetti di livello inferiore e interfacce in OLE. Le interfacce esatte disponibili in un controllo variano in base alle relative funzionalità. In questa sezione vengono esaminate in dettaglio le funzionalità che possono essere fornite da un controllo.

I controlli ActiveX vengono utilizzati per fornire i blocchi predefiniti per la creazione di interfacce utente nelle applicazioni. Ad esempio, un pulsante che avvia un'azione nell'applicazione contenitore quando viene selezionato è un controllo semplice. Per fornire questi blocchi predefiniti dell'interfaccia utente sono necessari gli aspetti seguenti:

-   È possibile incorporare un controllo all'interno del client contenitore per supportare alcune attività dell'interfaccia utente all'interno del client. Pertanto, un controllo deve fornire una rappresentazione visiva di se stesso quando viene incorporato all'interno del contenitore e deve fornire un modo per salvarne lo stato, ad esempio i valori delle proprietà e la posizione all'interno del relativo contenitore. Il client deve supportare un contenitore con oggetti incorporati.
-   Attivando il controllo utilizzando una tastiera o un mouse, l'utente finale avvia un'azione nell'applicazione client. Pertanto, un controllo deve rispondere all'attività della tastiera e deve essere in grado di comunicare con il client in modo che possa inviare notifiche al contenitore delle attività e attivare gli eventi nel client.
-   Il client in genere fornisce anche un linguaggio di programmazione tramite il quale l'utente finale può avviare azioni fornite dalle proprietà e dai metodi del controllo. In questo modo, un controllo deve supportare l'automazione e alcuni set di funzionalità in fase di progettazione rispetto a quelle di Runtime.

Come conseguenza del suo ruolo nell'fornire blocchi predefiniti dell'interfaccia utente, un controllo in genere supporta le funzionalità nelle seguenti aree usando le tecnologie OLE come indicato:

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Proprietà e metodi
</dt> <dd>

Analogamente a qualsiasi oggetto OLE, un controllo può offrire gran parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi. Il contenitore può fornire proprietà di ambiente aggiuntive e può supportare l'estensione delle proprietà del controllo tramite l'aggregazione. Queste funzionalità restano in automazione OLE, pagine delle proprietà, oggetti collegabili e tecnologie di controllo ActiveX.

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Eventi
</dt> <dd>

Oltre a fornire proprietà e metodi, un controllo ActiveX può anche fornire interfacce in uscita per notificare al client gli eventi. Il client deve supportare la gestione di questi eventi. Queste funzionalità usano l'automazione OLE e gli oggetti collegabili.

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Rappresentazione visiva
</dt> <dd>

Un controllo può supportare il posizionamento e la visualizzazione all'interno del relativo contenitore. Il contenitore posiziona il controllo e ne determina la dimensione. Queste funzionalità utilizzano la tecnologia per documenti compositi, inclusa la tecnologia di trascinamento della selezione OLE.

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Gestione della tastiera
</dt> <dd>

Un controllo può rispondere agli acceleratori della tastiera, in modo che l'utente finale possa avviare le azioni eseguite dal controllo. Il contenitore gestisce l'attività della tastiera per tutti i controlli incorporati. Queste funzionalità utilizzano le tecnologie di controllo e di documento composto.

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistenza
</dt> <dd>

Un controllo può salvare il proprio stato. Il client gestisce la persistenza dei controlli incorporati. Queste funzionalità utilizzano le tecnologie di archiviazione strutturata e di persistenza degli oggetti.

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registrazione e licenze
</dt> <dd>

Un controllo in genere supporta la registrazione automatica e crea un set di voci del registro di sistema quando ne viene creata un'istanza. Un controllo può anche essere concesso in licenza per impedire l'uso non autorizzato.

</dd> </dl>

La maggior parte di queste funzionalità coinvolgono sia il controllo che il relativo contenitore client.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> </dl>

 

 




