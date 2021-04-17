---
title: Pattern di controllo Annotation
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IAnnotationProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo Annotation viene usato per esporre le proprietà di un'annotazione in un documento.
ms.assetid: 5A334991-66AF-4A82-9A09-09D5BDAAA771
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo Annotation
- Automazione interfaccia utente, pattern di controllo Annotation
- Automazione interfaccia utente, IAnnotationProvider
- IAnnotationProvider
- implementazione del pattern di controllo Annotation di automazione interfaccia utente
- pattern di controllo Annotation
- pattern di controllo, IAnnotationProvider
- pattern di controllo, implementazione dell'annotazione automazione interfaccia utente
- pattern di controllo, annotazione
- interfacce, IAnnotationProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a0441816e548faaa9076b3a9717c0aa76f08a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300060"
---
# <a name="annotation-control-pattern"></a>Pattern di controllo Annotation

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **annotation** viene usato per esporre le proprietà di un'annotazione in un documento.

Un esempio è un fumetto di commento che si trova nel margine di un documento ed è connesso a un testo del documento o a una cella di un foglio di calcolo.

Nell'illustrazione seguente viene illustrato un esempio di un'annotazione. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

![screenshot che mostra un commento baloon in un documento](images/annotation.png)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IAnnotationProvider**](#required-members-for-iannotationprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **annotation** , tenere presenti le linee guida e le convenzioni seguenti:

-   Esistono molti tipi diversi di annotazioni. Il file di intestazione UIAutomationClient. h definisce un set di valori costanti denominati che identificano i tipi di annotazioni supportati da automazione interfaccia utente Microsoft. Per altre informazioni, vedere [**identificatori dei tipi di annotazione**](uiauto-annotation-type-identifiers.md).
-   Se si usa [**AnnotationType \_ Unknown**](uiauto-annotation-type-identifiers.md), è necessario implementare la proprietà [**IAnnotationProvider:: AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) per consentire ai client di individuare il nome del tipo di annotazione. Non è necessario implementare **AnnotationTypeName** per un tipo di annotazione standard perché automazione interfaccia utente fornisce un nome predefinito, ma è possibile implementarlo se è necessario eseguire l'override del nome predefinito.
-   La proprietà [**IAnnotationProvider:: Author**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author) è facoltativa.
-   La proprietà [**IAnnotationProvider::D atetime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime) è facoltativa.
-   La proprietà [**IAnnotationProvider:: target**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target) è obbligatoria perché collega un'annotazione a un elemento dell'interfaccia utente, consentendo a un client di spostarsi dall'annotazione all'elemento dell'interfaccia utente a cui si riferisce l'annotazione.
-   Poiché le annotazioni possono assumere molti formati diversi, l'interfaccia [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) non definisce una proprietà per archiviare il valore o il testo di un'annotazione. Un'annotazione semplice deve esporre l'interfaccia [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) e la proprietà [**IValueProvider:: value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deve restituire un valore di sola lettura che specifica il testo dell'annotazione. Un'annotazione più dettagliata deve esporre l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) per fornire un testo più completo ai client.
-   Lo spostamento da un elemento dell'interfaccia utente a un'annotazione sull'elemento dipende dal tipo di elemento annotato, come indicato di seguito:
    -   Per le celle del foglio di calcolo, implementare il metodo [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) per fare riferimento all'annotazione.
    -   Per il contenuto testuale, implementare l'attributo di testo [**AnnotationObjects**](uiauto-textattribute-ids.md) nell'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) per fare riferimento all'annotazione.
-   Alcuni tipi di annotazioni non richiedono un'implementazione completa dell'interfaccia [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Ad esempio, un indicatore di errore di ortografia semplice può essere rappresentato facendo in modo che l'interfaccia [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) restituisca un attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) di [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)e un valore null per l'attributo di testo [**AnnotationObjects**](uiauto-textattribute-ids.md) .
-   Può essere utile implementare l'interfaccia [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) su un elemento dell'interfaccia utente che non è visibile. Ad esempio, è possibile creare un elemento di automazione interfaccia utente non visibile che implementi **IAnnotationProvider** per fornire informazioni estese su un errore di grammatica.
-   Le annotazioni in un controllo basato su testo possono essere complesse se il controllo contiene commenti sovrapposti. Usare le linee guida seguenti per gestire le annotazioni complesse:
    -   Un intervallo di testo senza annotazioni deve restituire una matrice vuota per l'attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) e una matrice vuota per l'attributo di testo [**AnnotationObjects**](uiauto-textattribute-ids.md) .
    -   Un intervallo di testo con un'annotazione deve restituire una matrice di un valore integer per l'attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) e una matrice di un'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per l'attributo di testo [**AnnotationObjects**](uiauto-textattribute-ids.md) .
    -   Un intervallo di testo con più annotazioni deve restituire una matrice di più valori integer per l'attributo di testo [**AnnotationTypes**](uiauto-textattribute-ids.md) e una matrice di un numero corrispondente di interfacce [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per l'attributo di testo [**AnnotationObjects**](uiauto-textattribute-ids.md) .
    -   Un intervallo di testo con annotazioni variabili, ad esempio un intervallo con testo con annotazioni e senza annotazioni, deve restituire la proprietà [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) sia per [**AnnotationTypes**](uiauto-textattribute-ids.md) che per [**AnnotationObjects**](uiauto-textattribute-ids.md). Un client che riceve questa risposta può suddividere l'intervallo di testo per individuare il punto in cui iniziano e terminano le annotazioni.

## <a name="required-members-for-iannotationprovider"></a>Membri obbligatori per **IAnnotationProvider**

Le proprietà seguenti sono necessarie per l'implementazione dell'interfaccia [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .



| Membri obbligatori                                                                | Tipo di membro | Note |
|---------------------------------------------------------------------------------|-------------|-------|
| [**AnnotationTypeId**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypeid)     | Proprietà    | Nessuna. |
| [**AnnotationTypeName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_annotationtypename) | Proprietà    | Nessuna. |
| [**Autore**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_author)                         | Proprietà    | Nessuna. |
| [**DateTime**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_datetime)                     | Proprietà    | Nessuna. |
| [**Destinazione**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iannotationprovider-get_target)                         | Proprietà    | Nessuna. |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> </dl>

 

 