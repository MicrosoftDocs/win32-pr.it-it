---
title: Modifica della proprietà del plug-in audio DSP di esempio
description: Modifica della proprietà del plug-in audio DSP di esempio
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in DSP audio, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712184"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Modifica della proprietà del plug-in audio DSP di esempio

È probabile che si desideri modificare la proprietà creata dalla procedura guidata plug-in di Windows Media Player per impostazione predefinita. Nell'elenco seguente vengono illustrati in dettaglio gli elementi che potrebbero richiedere modifiche:

-   **Risorsa della finestra di dialogo.** Fare clic sulla scheda **ResourceView** nella finestra dell'area di lavoro progetto. Espandere l'elenco di cartelle per aprire la cartella della finestra di dialogo. Fare doppio clic sulla risorsa finestra di dialogo per aprire l'editor risorse. È possibile apportare modifiche alla finestra di dialogo della pagina delle proprietà per soddisfare le proprie esigenze. Ad esempio, è possibile modificare il testo nell'etichetta o sostituire il controllo di modifica con una casella di controllo.
-   **Codice dell'oggetto della pagina delle proprietà.** L'implementazione predefinita usa una variabile di tipo Double per archiviare il fattore di scala. Potrebbe essere necessario un tipo di dati diverso. Questa operazione richiede anche la modifica del codice che rende permanente i dati nel registro di sistema e legge i dati dal registro di sistema (incluso il codice che legge dal registro di sistema in *CProjectName*::**FinalConstruct**).
-   **Variabile membro che archivia il valore della proprietà.** Questa variabile è denominata "m \_ fScaleFactor" ed è dichiarata come tipo Double. Potrebbe essere necessario modificare il nome e il tipo di questa variabile in tutto il progetto.
-   **Metodi get e Property put della proprietà.** Potrebbe essere necessario modificare i nomi, i parametri e le implementazioni di questi metodi. Non dimenticare di riflettere anche le modifiche apportate altrove nel progetto. Ad esempio, la pagina delle proprietà **Apply** Method chiama *CProjectName*::**put \_ scale**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




