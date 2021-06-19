---
description: Informazioni sulle procedure consigliate per i gestori dei menu di scelta rapida e più verbi quando si implementa un formato di file personalizzato nella shell di Windows.
title: Procedure consigliate per gestori di menu di scelta rapida e più verbi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 14ec2e8915aa1df47ca21c6436ec963be3f590f5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396446"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Procedure consigliate per gestori di menu di scelta rapida e più verbi

Questo argomento è organizzato come segue:

-   [Procedure consigliate](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Procedure consigliate per le implementazioni di verbi](#best-practices-for-verb-implementations)
-   [Procedure consigliate per più verbi di selezione](#best-practices-for-multiple-selection-verbs)
    -   [Selezioni eterogenee](#heterogenous-selections)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

I verbi statici sono verbi più semplici da implementare e forniscono funzionalità avanzate. È consigliabile implementare un verbo usando uno dei metodi di verbi statici.

### <a name="best-practices-for-verb-implementations"></a>Procedure consigliate per le implementazioni di verbi

L'elenco seguente rappresenta le procedure consigliate per le implementazioni di verbi:

-   Scegliere sempre il metodo verbo più semplice che soddisfi le proprie esigenze.
-   Usare un metodo verbo statico, se possibile.
-   Non eseguire operazioni a elevato utilizzo di risorse o I/O nel thread dell'interfaccia utente. Sia [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) che [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) devono essere molto conservativi nel lavoro che eseguono. [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) deve essere eseguito in un altro processo oppure è necessario creare un nuovo thread per evitare di bloccare il chiamante.
-   Prefissi verbi con il nome del fornitore di software indipendente (ISV) come indicato di seguito, `ISVName.verb` . L'uso di nomi non qualificati può causare conflitti con più ISV che hanno scelto lo stesso nome di verbo.
-   Usare sempre un ProgID specifico dell'applicazione. Poiché alcuni tipi di elemento non usano questo mapping, è necessario usare nomi univoci del fornitore.
-   Posizionare l'interfaccia utente rispetto al metodo di chiamata, ma non eseguire su un thread invoker.
-   Non accettare il valore restituito **S \_ OK** per i verbi canonici passati al [**metodo IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) In questo modo viene richiamato un errore per l'implementazione effettiva del verbo e viene restituito un codice di errore per i verbi canonici. Se non si supportano verbi canonici, viene restituito un errore quando viene rilevato un valore HIWORD(lpVerb) diverso da zero.
-   Evitare l'uso **dirundll32.exe** come host per il verbo.
-   Quando si implementa [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) assicurarsi di restituire il numero di verbi aggiunti al menu tramite il valore **HRESULT** usando la macro ResultFromShort.
-   Se si registra in una delle voci di chiave del Registro di sistema seguenti, prestare attenzione e assicurarsi di registrare il gestore nel tipo più specifico per ridurre le conseguenze possibilmente impreviste:
    -   **RADICE DELLE \_ CLASSI \_ HKEY\\\***
    -   **HKEY \_ CLASSES \_ ROOT \\ AllFileSystemObjects**
    -   **Cartella RADICE HKEY \_ CLASSES \_ \\**
    -   **DIRECTORY RADICE DELLE CLASSI HKEY \_ \_ \\**
-   Impostare la **chiave MayChangeDefaultMenu** solo se si prevede che potrebbe essere necessario modificare il verbo predefinito nel menu di scelta rapida. Se il gestore non modifica il verbo predefinito, non è necessario impostare questa chiave perché in questo modo il sistema carica la DLL inutilmente.
-   Ridurre al minimo le operazioni eseguite in [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Per i gestori del menu di scelta rapida, acquisire l'oggetto dati passato a **IShellExtInit::Initialize** e quindi elaborarlo in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)o [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Procedure consigliate per più verbi di selezione

Poiché il numero di elementi in uno scenario con più verbi di selezione può essere elevato, è importante considerare le implicazioni in termini di prestazioni delle implementazioni dei verbi. Ad esempio, quando un utente cerca " " su un ambito che include un numero elevato di elementi e quindi fa clic su Seleziona tutto e fa clic con il pulsante destro del mouse, al verbo viene visualizzata una selezione che può contenere migliaia di \* elementi.  Di conseguenza, i verbi devono considerare solo il primo elemento nella selezione e il conteggio complessivo degli elementi. Il primo elemento viene definito come elemento nella parte superiore della visualizzazione o come elemento su cui l'utente ha fatto clic con il pulsante destro del mouse.

In Windows 7 e versioni successive, il numero di elementi passati a un verbo è limitato a 16 quando viene eseguita una query su un menu di scelta rapida. Il verbo viene quindi ri-creato e inizializzato nuovamente con la selezione completa quando tale verbo viene richiamato.

In alcuni casi è opportuno prendere in considerazione un numero ridotto di elementi fissi. Ad esempio, è appropriato che un verbo "diff" consideri solo i primi due elementi. In genere, non è necessario testare ogni elemento nella selezione per verificare se si tratta di un determinato tipo o eseguire una query su ogni elemento nella selezione per le relative proprietà. Esaminare invece il primo elemento e decidere se è appropriato aggiungere il verbo.

### <a name="heterogenous-selections"></a>Selezioni eterogenee

I verbi ottimistici vengono aggiunti automaticamente nel caso a selezione multipla, presupponendo che gli elementi non selezionati possano essere gestiti dal verbo. Al contrario, i verbi pessimistici non vengono aggiunti quando la selezione contiene elementi non selezionati e vengono aggiunti solo nei casi in cui il numero di elementi è ridotto.

I verbi di stile del lettore devono essere ottimistici e ignorare automaticamente gli elementi non gestiti. Se un errore di azione sugli elementi può causare perdita di dati o confusione, il verbo deve avvisare gli utenti degli elementi che non possono essere elaborati. Ad esempio, un verbo di "backup" deve indicare che non è stato possibile eseguire il backup di alcuni elementi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Informazioni di riferimento sul menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 



