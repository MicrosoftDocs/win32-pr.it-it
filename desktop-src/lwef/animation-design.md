---
title: Progettazione di animazioni
description: Progettazione di animazioni
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225a500d94b4de6f9133650a6aed415a49329585bc9bc9f83dec028668e51215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752292"
---
# <a name="animation-design"></a>Progettazione di animazioni

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

### <a name="image-design"></a>Progettazione di immagini

Usare il riquadro Microsoft Office quando si progettano i caratteri per ridurre al minimo eventuali problemi di realizzazione del riquadro. Evitare di selezionare un colore di trasparenza simile ai colori utilizzati nel documento.

### <a name="sounds"></a>Suoni

Microsoft Agent consente di riprodurre suoni nelle animazioni. È consigliabile non includere  suoni per le animazioni inattive. In questo modo non si verifica un ritardo nel mezzo dell'animazione, se Agent deve caricare la DLL multimediale di sistema.

### <a name="frame-size"></a>Dimensioni fotogramma

Gli assistenti Office sono tipici di 123 x 93 pixel. Anche se è possibile creare caratteri di altre dimensioni, verranno ridimensionati a 123 x 93 nella Raccolta assistenti.

### <a name="frame-transition"></a>Transizione di frame

Tutte le animazioni ad eccezione **di Goodbye,** **Greeting,** **Show** e **Hide** devono iniziare e terminare con l'animazione RestPose. Microsoft Office non riproduce animazioni **return** esplicite, pertanto non è consigliabile definirle. Anche tutte le animazioni devono avere Exit Branching. La diramazione di uscita consente di "sbrigare e terminare" l'animazione corrente prima di chiamare l'animazione successiva. Se non si specifica Exit Branching, la transizione tra animazioni può risultare a scatti.

### <a name="character-properties"></a>Proprietà carattere

Microsoft Agent consente di impostare le proprietà [**Name**](name-property.md), [**Description**](description-property.md) [**ed ExtraData del**](extradata-property.md) carattere. Microsoft Office usa il **campo ExtraData** per contenere una o più frasi introduttive e frasi di promemoria. Microsoft Office le altre frasi introduttive da inserire nel fumetto della raccolta di assistenti. Le frasi di promemoria vengono usate quando si riceve un promemoria da Outlook.

Il [**campo ExtraData**](extradata-property.md) viene formattato come segue:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

Le frasi introduttive sono separate da una coppia di caratteri tilde (~), seguite da frasi di promemoria. Queste frasi di promemoria sono separate anche da una coppia di caratteri tilde. I due set di frasi sono separati da due caratteri di (^^). Non esiste alcun limite al numero di ogni tipo di frase, ad eccezione del fatto che deve essere presente almeno uno di essi.

 

 




