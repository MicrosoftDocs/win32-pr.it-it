---
description: 'Questo argomento è organizzato nel modo seguente:'
title: Procedure consigliate per i gestori di menu di scelta rapida e più verbi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f8b47807c4647aec274e64dbcd137833d13e23cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980215"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Procedure consigliate per i gestori di menu di scelta rapida e più verbi

Questo argomento è organizzato nel modo seguente:

-   [Procedure consigliate](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Procedure consigliate per le implementazioni di verbi](#best-practices-for-verb-implementations)
-   [Procedure consigliate per più verbi di selezione](#best-practices-for-multiple-selection-verbs)
    -   [Selezioni eterogeneo](#heterogenous-selections)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

Il verbo statico è costituito da verbi più semplici da implementare e fornisce funzionalità avanzate. Si consiglia di implementare un verbo usando uno dei metodi del verbo statico.

### <a name="best-practices-for-verb-implementations"></a>Procedure consigliate per le implementazioni di verbi

L'elenco seguente rappresenta le procedure consigliate per le implementazioni dei verbi:

-   Scegliere sempre il metodo verbo più semplice che soddisfi le proprie esigenze.
-   Usare un metodo verbo statico, se possibile.
-   Non eseguire operazioni con utilizzo intensivo di risorse o I/O sul thread UI. Sia [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) che [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) devono essere molto prudenti nel lavoro che eseguono. [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) deve essere eseguito in un altro processo oppure è necessario creare un nuovo thread per evitare il blocco del chiamante.
-   Anteporre i verbi al nome del fornitore di software indipendente (ISV), come indicato di seguito `ISVName.verb` . L'utilizzo di nomi non qualificati può comportare conflitti con più ISV che scelgono lo stesso nome verbo.
-   Usare sempre un ProgID specifico dell'applicazione. Poiché alcuni tipi di elemento non utilizzano questo mapping, è necessario disporre di nomi univoci del fornitore.
-   Posizionare l'interfaccia utente rispetto al metodo chiamante, ma non eseguire su un thread invoker.
-   Non accettare il valore restituito **S \_ OK** per i verbi canonici passati al metodo [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . In questo modo viene generato un errore per l'implementazione del verbo reale da richiamare e viene restituito un codice di errore per i verbi canonici. Se non sono supportati verbi canonici, restituire un errore quando viene rilevato un valore diverso da zero HIWORD (lpVerb).
-   Evitare l'uso di **rundll32.exe** come host per il verbo.
-   Quando si implementa [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , assicurarsi di restituire il numero di verbi aggiunti al menu tramite il valore **HRESULT** utilizzando la macro ResultFromShort.
-   Se si esegue la registrazione su una delle seguenti voci della chiave del registro di sistema, prestare attenzione e assicurarsi di registrare il gestore sul tipo più specifico per ridurre le conseguenze probabilmente non intenzionali:
    -   **HKEY \_ \_ \\ radice \* classi* _
    -   _ *HKEY \_ classi \_ radice \\ AllFileSystemObjects**
    -   **\_ \_ Cartella radice delle classi HKEY \\**
    -   **\_ \_ Directory radice delle classi HKEY \\**
-   Impostare la chiave **MayChangeDefaultMenu** solo se si prevede che potrebbe essere necessario modificare il verbo predefinito nel menu di scelta rapida. Se il gestore non modifica il verbo predefinito, è consigliabile non impostare questa chiave perché in questo modo il sistema carica la DLL inutilmente.
-   Ridurre al minimo le operazioni eseguite in [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Per i gestori di menu di scelta rapida, acquisire l'oggetto dati passato a **IShellExtInit:: Initialize**, quindi elaborarlo in [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Procedure consigliate per più verbi di selezione

Poiché il numero di elementi in uno scenario con più verbi di selezione può essere di grandi dimensioni, è importante considerare le implicazioni sulle prestazioni delle implementazioni dei verbi. Ad esempio, quando un utente cerca " \* " su un ambito che include un numero elevato di elementi e quindi fa clic su **Seleziona tutto** e fa clic con il pulsante destro del mouse, il verbo viene visualizzato con una selezione che può contenere migliaia di elementi. Di conseguenza, i verbi devono considerare solo il primo elemento della selezione e il numero complessivo di elementi. Il primo elemento è definito come l'elemento nella parte superiore della visualizzazione o l'elemento su cui l'utente ha fatto clic con il pulsante destro del mouse.

In Windows 7 e versioni successive, il numero di elementi passati a un verbo è limitato a 16 quando viene eseguita una query su un menu di scelta rapida. Il verbo viene quindi ricreato e inizializzato nuovamente con la selezione completa quando viene richiamato il verbo.

In alcuni casi è opportuno prendere in considerazione un numero ridotto di elementi fissi. Ad esempio, è opportuno che un verbo "diff" consideri solo i primi due elementi. In genere, non è necessario testare ogni elemento della selezione per verificare se è un determinato tipo oppure eseguire una query su ogni elemento della selezione per le relative proprietà. Si osservi invece il primo elemento e decidere se è appropriato aggiungere il verbo.

### <a name="heterogenous-selections"></a>Selezioni eterogeneo

I verbi ottimistici vengono aggiunti automaticamente nel case di selezione, presupponendo che gli elementi non controllati possano essere gestiti dal verbo. Al contrario, i verbi pessimistici non vengono aggiunti quando la selezione contiene elementi non controllati e vengono aggiunti solo nei casi in cui il numero di elementi è ridotto.

I verbi di stile del lettore devono essere ottimisti e ignorare automaticamente gli elementi che non vengono gestiti. Se un errore di agire sugli elementi può causare la perdita o la confusione dei dati, il verbo deve avvertire gli utenti degli elementi che non possono essere elaborati. Ad esempio, un verbo "backup" indica che non è stato possibile eseguire il backup di alcuni elementi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida (contesto) e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Riferimento al menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 



