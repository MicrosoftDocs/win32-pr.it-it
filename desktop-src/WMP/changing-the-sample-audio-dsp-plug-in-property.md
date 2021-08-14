---
title: Modifica della proprietà del plug-in Audio DSP di esempio
description: Modifica della proprietà del plug-in Audio DSP di esempio
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player plug-in, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione del segnale digitale, proprietà audio
- Plug-in DSP, proprietà audio
- plug-in DSP audio,proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342624"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Modifica della proprietà del plug-in Audio DSP di esempio

È probabile che si voglia modificare la proprietà creata per impostazione Windows Media Player guidata plug-in. L'elenco seguente elenca in dettaglio gli elementi che potrebbero richiedere la modifica:

-   **Risorsa della finestra di dialogo.** Fare clic **sulla scheda ResourceView** nella finestra dell Project workspace. Espandere l'elenco di cartelle per aprire la cartella Finestra di dialogo. Fare doppio clic sulla risorsa finestra di dialogo per aprire l'editor di risorse. È possibile apportare modifiche alla finestra di dialogo della pagina delle proprietà per soddisfare le proprie esigenze. Ad esempio, è possibile modificare il testo nell'etichetta o sostituire il controllo di modifica con una casella di controllo.
-   **Codice dell'oggetto della pagina delle proprietà.** L'implementazione predefinita usa una variabile di tipo double per archiviare il fattore di scala. Potrebbe essere necessario un tipo di dati diverso. Ciò richiederebbe anche di modificare il codice che rende persistenti i dati nel Registro di sistema e legge i dati dal Registro di sistema (incluso il codice che legge dal Registro di sistema in *CProjectName*::**FinalConstruct**).
-   **Variabile membro che archivia il valore della proprietà.** Questa variabile è denominata "m \_ fScaleFactor" ed è dichiarata come tipo double. È possibile modificare il nome e il tipo di questa variabile in tutto il progetto.
-   **I metodi property get e property put.** È possibile modificare i nomi, i parametri e le implementazioni di questi metodi. Non dimenticare di riflettere anche queste modifiche altrove nel progetto. Ad esempio, il metodo **Apply della pagina delle** proprietà chiama *CProjectName*::**put \_ scale**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




