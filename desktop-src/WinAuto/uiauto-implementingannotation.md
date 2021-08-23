---
title: Pattern di controllo Annotation
description: Descrive le linee guida e le convenzioni per l'implementazione di IAnnotationProvider, incluse le informazioni su proprietà e metodi. Il pattern di controllo Annotation viene usato per esporre le proprietà di un'annotazione in un documento.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo annotation
- Automazione interfaccia utente,pattern di controllo annotation
- Automazione interfaccia utente,IAnnotationProvider
- IAnnotationProvider
- implementazione di Automazione interfaccia utente pattern di controllo annotation
- Pattern di controllo annotation
- pattern di controllo, IAnnotationProvider
- pattern di controllo, implementazione di Automazione interfaccia utente annotazione
- pattern di controllo, annotazione
- interfacce, IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cdc5c37c61878513b5d01812ab73c086f87d182d4b2c955efaf8706d52e4bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505257"
---
# <a name="annotation-control-pattern"></a>Pattern di controllo Annotation

Descrive le linee guida e le convenzioni per l'implementazione [**di IAnnotationProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)incluse le informazioni su proprietà e metodi. Il **pattern di** controllo Annotation viene usato per esporre le proprietà di un'annotazione in un documento.

Un esempio è un fumetto di commento che si trova sul margine di un documento ed è connesso a un testo del documento o a una cella del foglio di calcolo.

Nella figura seguente viene illustrato un esempio di annotazione. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

![Screenshot che mostra un commento in un documento](images/annotation.png)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IAnnotationProvider**](#required-members-for-iannotationprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Annotation,** tenere presente le linee guida e le convenzioni seguenti:

-   Esistono molti tipi diversi di annotazioni. Il file di intestazione UIAutomationClient.h definisce un set di valori costanti denominati che identificano i tipi di annotazioni supportati da Microsoft Automazione interfaccia utente. Per altre informazioni, vedere [**Identificatori dei tipi di annotazione.**](uiauto-annotation-type-identifiers.md)
-   Se si usa [**AnnotationType \_ Unknown,**](uiauto-annotation-type-identifiers.md)è necessario implementare la proprietà [**IAnnotationProvider::AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) per consentire ai client di individuare il nome del tipo di annotazione. Non è necessario implementare **AnnotationTypeName** per un tipo di annotazione standard perché Automazione interfaccia utente fornisce un nome predefinito, ma è possibile implementarlo se è necessario eseguire l'override del nome predefinito.
-   La [**proprietà IAnnotationProvider::Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) è facoltativa.
-   La [**proprietà IAnnotationProvider::D ateTime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) è facoltativa.
-   La [**proprietà IAnnotationProvider::Target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) è obbligatoria perché collega un'annotazione a un elemento dell'interfaccia utente, consentendo a un client di tornare dall'annotazione all'elemento dell'interfaccia utente a cui fa riferimento l'annotazione.
-   Poiché le annotazioni possono assumere forme diverse, [**l'interfaccia IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) non definisce una proprietà per l'archiviazione del valore o del testo di un'annotazione. Un'annotazione semplice deve esporre l'interfaccia [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) e la proprietà [**IValueProvider::Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deve restituire un valore di sola lettura che specifica il testo dell'annotazione. Un'annotazione più ricca deve esporre [**l'interfaccia ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) per fornire testo più rtf ai client.
-   Lo spostamento da un elemento dell'interfaccia utente a un'annotazione sull'elemento dipende dal tipo di elemento annotato, come indicato di seguito:
    -   Per le celle del foglio di calcolo, implementare il metodo [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) per fare riferimento all'annotazione.
    -   Per il contenuto testuale, implementare l'attributo di testo [**AnnotationObjects**](uiauto-textattribute-ids.md) [**nell'interfaccia ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) per fare riferimento all'annotazione.
-   Alcuni tipi di annotazioni non richiedono un'implementazione completa [**dell'interfaccia IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) Ad esempio, un semplice indicatore di errore di ortografia può essere rappresentato facendo in modo che l'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) restituisci un attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) di [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e un valore Null per l'attributo di testo [**AnnotationObjects.**](uiauto-textattribute-ids.md)
-   Può essere utile implementare [**l'interfaccia IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) in un elemento dell'interfaccia utente non visibile. Ad esempio, è possibile creare un elemento Automazione interfaccia utente non visibile che implementa **IAnnotationProvider** per fornire informazioni estese su un errore di grammatica.
-   Le annotazioni in un controllo basato su testo possono essere complesse se il controllo contiene commenti sovrapposti. Usare le linee guida seguenti per gestire annotazioni complesse:
    -   Un intervallo di testo senza annotazioni deve restituire una matrice vuota per l'attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) e una matrice vuota per l'attributo di testo [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Un intervallo di testo con un'annotazione deve restituire una matrice di un valore intero per l'attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) e una matrice di [**un'interfaccia IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per l'attributo di testo [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Un intervallo di testo con più annotazioni deve restituire una matrice di più valori integer per l'attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) e una matrice di un numero corrispondente di interfacce [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per l'attributo di testo [**AnnotationObjects.**](uiauto-textattribute-ids.md)
    -   Un intervallo di testo con annotazioni variabili, ad esempio un intervallo con testo con annotazioni e testo non annotato, deve restituire la proprietà [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) sia per [**AnnotationTypes**](uiauto-textattribute-ids.md) che per [**AnnotationObjects.**](uiauto-textattribute-ids.md) Un client che riceve questa risposta può suddividere l'intervallo di testo per trovare dove iniziano e terminano le annotazioni.

## <a name="required-members-for-iannotationprovider"></a>Membri obbligatori per **IAnnotationProvider**

Le proprietà seguenti sono necessarie per l'implementazione [**dell'interfaccia IAnnotationProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider)



| Membri obbligatori                                                                | Tipo di membro | Note |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Proprietà    | Nessuno. |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Proprietà    | Nessuno. |
| [**Autore**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Proprietà    | Nessuno. |
| [**Datetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Proprietà    | Nessuno. |
| [**Destinazione**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Proprietà    | Nessuno. |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e relativi pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 