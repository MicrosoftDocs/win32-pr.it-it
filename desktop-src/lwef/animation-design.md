---
title: Progettazione dell'animazione
description: Progettazione dell'animazione
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955351"
---
# <a name="animation-design"></a>Progettazione dell'animazione

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="image-design"></a>Progettazione immagine

Usare la tavolozza Microsoft Office durante la progettazione dei caratteri per ridurre al minimo i potenziali problemi di realizzazione della tavolozza. Evitare di selezionare un colore di trasparenza simile ai colori usati nel documento.

### <a name="sounds"></a>Suoni

Microsoft Agent consente di riprodurre suoni nelle animazioni. Si consiglia di non includere suoni per le animazioni **inattive** . In questo modo, se l'agente deve caricare la DLL multimediale di sistema, non si verifica alcun ritardo al centro dell'animazione.

### <a name="frame-size"></a>Dimensioni frame

Gli assistenti di Office tipici sono 123 x 93 pixel. Sebbene sia possibile creare caratteri di altre dimensioni, questi verranno ridimensionati a 123 x 93 nella raccolta di assistenti.

### <a name="frame-transition"></a>Transizione del frame

Tutte le animazioni eccetto **Goodbye**, **Greeting**, **show** e **Hide** devono iniziare e terminare con l'animazione RestPose. Microsoft Office non riproduce animazioni di **restituzione** esplicite, pertanto non è necessario definirle. Tutte le animazioni devono anche avere una diramazione di uscita. Exit Branching consente di affrettare e completare l'animazione corrente prima di chiamare l'animazione successiva. Se non si fornisce la diramazione di uscita, la transizione tra le animazioni potrebbe essere Jerky.

### <a name="character-properties"></a>Proprietà carattere

Microsoft Agent consente di impostare il [**nome**](name-property.md), la [**Descrizione**](description-property.md) e le proprietà [**dei dati**](extradata-property.md) di tipo carattere. Microsoft Office utilizza il campo **dei dati** di prima per conservare una o più frasi introduttive e frasi di promemoria. Microsoft Office preleva dalle altre frasi introduttive da inserire nell'aerostato vocale della raccolta di assistenti. Le frasi promemoria vengono usate quando si riceve un promemoria da Outlook.

Il campo [**dati**](extradata-property.md) non è formattato come segue:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

Le frasi introduttive sono separate da una coppia di caratteri tilde (~), seguite da frasi di promemoria. Queste frasi di promemoria sono separate anche da una coppia di caratteri tilde. I due set di frasi sono separati da due caratteri di accento (^^). Non esiste alcun limite al numero di ogni tipo di frase, ad eccezione del fatto che deve essere presente almeno uno di essi.

 

 




