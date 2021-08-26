---
description: È in genere consigliabile copiare un set di informazioni più complesso di quello che può essere contenuto nel formato ISF (Ink Serialized Format).
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Archiviazione dell'input penna in HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8949582c5743ba7be5ac664627792c7b7f8a0cd5968a67f5db08b6428cb886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934361"
---
# <a name="storing-ink-in-html"></a>Archiviazione dell'input penna in HTML

È in genere consigliabile copiare un set di informazioni più complesso di quello che può essere contenuto nel formato ISF (Ink Serialized Format). HTML è particolarmente utile come formato di interoperabilità a causa della sua forte accettazione come standard di settore e della capacità di rappresentare contenuto eterogeneo.

HTML è ampiamente noto, ben documentato e familiare a molti sviluppatori. Sono disponibili molti strumenti per la produzione HTML. Inoltre, Microsoft Windows contiene API (Application Programming Interface) per il rendering e la manipolazione del codice HTML. Infine, le API della piattaforma Tablet PC forniscono il formato di persistenza GIF semplificato, adatto per l'incorporamento in altri formati, soprattutto HTML. Questo formato è costituito da un file GIF con Ink Serialized Format (ISF) incorporato in un blocco di estensione dell'applicazione.

Questi file GIF sono rappresentazioni di oggetti input penna che:

-   Eseguire il rendering in applicazioni non abilitate per l'input penna, ad esempio browser o elaboratori di testo legacy.
-   Contiene tutte le informazioni necessarie dall'input penna originale che si vuole mantenere per scopi quali la modifica o il riconoscimento.

Questi file GIF possono essere prodotti usando i metodi di persistenza delle API della piattaforma Tablet PC. Si tratta di GIF e devono usare l'estensione GIF e, per un'applicazione non abilitata per l'input penna, non c'è nulla di diverso da una normale GIF. Per un'applicazione abilitata per l'input penna, tuttavia, è disponibile un set di dati ricco sottostante l'immagine.

Dopo che è stata prodotta dalle API della piattaforma Tablet PC, un tag IMG in HTML fa riferimento a una GIF unificata. Il codice HTML viene quindi archiviato nello slot degli Appunti \_ HTML cf standard. In questo modo il codice HTML può essere visibile ad altre applicazioni, indipendentemente dal fatto che siano abilitate per l'input penna. L'immagine stessa può essere archiviata nella cache Windows Internet e impostata per il timeout dopo un periodo di tempo appropriato.

Sono disponibili o obbligatorie aree di controllo specifiche per il tag IMG. Queste aree di controllo identificano il codice HTML come contenitore dell'input penna. L'esempio seguente fa riferimento a una GIF unificata usando tag HTML:

`<img href="34372423432.gif" />`

Se è necessario fare riferimento all'immagine con altri mezzi, ad esempio fogli di stile CSS o Vector Markup Language (VML), dovrebbe essere ancora presente un tag IMG che fa riferimento all'immagine. In questo modo è possibile tagliare e incollare da e verso qualsiasi applicazione che accetta rappresentazioni HTML dell'input penna.

Le applicazioni che supportano l'input penna in HTML devono:

-   Generare codice \_ HTML CF quando l'utente esegue una copia. Quando si genera codice HTML CF durante la copia (o il salvataggio in formato HTML), usare il metodo \_ [Microsoft.Ink.Ink.Save,](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) specificando il valore [Microsoft.Ink.PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) nel *parametro p,* per generare un'immagine GIF unificata. Il testo alternativo deve essere impostato sul risultato del riconoscimento più accurato. È possibile impostare il posizionamento su assoluto o sul posto, in base alle esigenze.
-   Controllare tutti i tag IMG per determinare se sono presenti immagini a cui puntano per contenere l'input penna, se lo slot HTML CF \_ viene scelto per un'operazione Incolla. In tal caso, considerare le immagini come [oggetti Ink](/previous-versions/aa515768(v=msdn.10)) internamente. Anche se in questa versione sono supportati solo file GIF, l'applicazione deve controllare anche le immagini non GIF, nel caso in cui in futuro siano supportati formati di immagine aggiuntivi.
-   Supportare la copia e incolla di ISF. Le applicazioni che supportano HTML devono supportare anche ISF per migliorare l'interoperabilità con le applicazioni abilitate all'input penna che non riconoscono HTML. Questa convenzione è simile alla convenzione in cui anche le applicazioni che posizionano codice HTML negli Appunti posizionano il testo.

Per altre informazioni sulle GIF arricchite, vedere [Blocchi predefiniti.](building-blocks.md)

 

 
