---
description: È in genere consigliabile copiare un set di informazioni più complesso rispetto a quello che può essere contenuto nel formato ISF (Ink Serialized Format).
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Archiviazione dell'input penna in HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372e6e77ea0284bc44fa70883964e53b3063bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315550"
---
# <a name="storing-ink-in-html"></a>Archiviazione dell'input penna in HTML

È in genere consigliabile copiare un set di informazioni più complesso rispetto a quello che può essere contenuto nel formato ISF (Ink Serialized Format). Il codice HTML è particolarmente utile come formato di interoperabilità grazie alla sua accettazione avanzata come standard di settore e alla possibilità di rappresentare contenuto eterogeneo.

HTML è ampiamente comprensibile, ben documentato e familiare a molti sviluppatori. Sono disponibili molti strumenti per la produzione HTML. Inoltre, Microsoft Windows contiene le API (Application Programming Interface) per il rendering e la manipolazione del codice HTML. Infine, le API della piattaforma Tablet PC forniscono il formato di persistenza GIF fortificato, che è adatto per l'incorporamento in altri formati, più importante in HTML. Questo formato è costituito da un file GIF con formato ISF (Ink Serialized Format) incorporato in un blocco dell'estensione dell'applicazione.

Questi file GIF sono rappresentazioni di oggetti Ink che:

-   Rendering in applicazioni che non sono abilitate per l'input penna, ad esempio browser o processori di Word legacy.
-   Contenere tutte le informazioni necessarie dall'input penna originale che si desidera mantenere per finalità quali la modifica o il riconoscimento.

Questi file GIF possono essere prodotti usando i metodi di persistenza delle API della piattaforma Tablet PC. Sono gif e devono usare l'estensione GIF e, per un'applicazione che non è abilitata per l'input penna, non c'è nulla di diverso da un GIF normale. In un'applicazione abilitata per l'input penna, tuttavia, esiste un set completo di dati sottostanti all'immagine.

Una volta prodotto dalle API della piattaforma Tablet PC, viene fatto riferimento a un GIF fortificato da un tag IMG in HTML. Il codice HTML viene quindi archiviato nello slot per gli \_ Appunti HTML CF standard. In questo modo il codice HTML può essere visibile ad altre applicazioni, indipendentemente dal fatto che siano abilitati per l'input penna. L'immagine stessa può essere archiviata nella cache Internet di Windows e impostata su Age out dopo un periodo di tempo appropriato.

Vengono fornite o richieste aree di modifica specifiche per il tag IMG. Queste aree di visualizzazione identificano il codice HTML che contiene l'input penna. L'esempio seguente fa riferimento a un GIF fortificato usando tag HTML:

`<img href="34372423432.gif" />`

Se è necessario fare riferimento all'immagine con altri mezzi, ad esempio fogli di stile CSS o Vector Markup Language (la), dovrebbe essere ancora presente un tag IMG che fa riferimento all'immagine. In questo modo è possibile tagliare e incollare all'interno e all'esterno di qualsiasi applicazione che accetti le rappresentazioni HTML dell'input penna.

Le applicazioni che supportano l'input penna in HTML devono:

-   Genera \_ il codice HTML CF quando l'utente esegue una copia. Quando si genera il \_ codice HTML CF in copia (o Salva come HTML), usare il metodo [Microsoft. Ink. Ink. Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) , specificando il valore [Microsoft. Ink. PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) nel parametro *p* , per generare un'immagine gif fortificata. Il testo alternativo deve essere impostato sul risultato del riconoscimento più preciso. È possibile impostare il posizionamento su assoluto o sul posto, a seconda delle esigenze.
-   Controllare tutti i tag IMG per determinare se le immagini a cui puntano contengono input penna, se è stata scelta l'opzione \_ per incollare il codice HTML CF. In tal caso, trattare le immagini come oggetti [Ink](/previous-versions/aa515768(v=msdn.10)) internamente. Sebbene in questa versione siano supportati solo i file GIF, l'applicazione deve controllare anche le immagini non GIF, nel caso in cui i formati di immagine aggiuntivi siano supportati in futuro.
-   Supporta la copia e incolla di ISF. Le applicazioni che supportano HTML devono inoltre supportare ISF per migliorare l'interoperabilità con applicazioni abilitate per l'input penna che non riconoscono HTML. Questa operazione è simile alla convenzione in cui anche le applicazioni che inseriscono HTML negli Appunti inseriscono testo.

Per altre informazioni sulle gif fortificate, vedere la pagina relativa ai [blocchi predefiniti](building-blocks.md).

 

 
