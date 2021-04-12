---
description: In questa sezione vengono fornite informazioni sulle interfacce utilizzate per controllare l'aspetto e il comportamento del pannello input penna di Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfacce del pannello di input di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233856"
---
# <a name="text-input-panel-interfaces"></a>Interfacce del pannello di input di testo

In questa sezione vengono fornite informazioni sulle interfacce utilizzate per controllare l'aspetto e il comportamento del pannello input penna di Tablet PC.

> [!Note]  
> Le interfacce del pannello di input di testo non sono conformi all'automazione.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Interfaccia                                                                | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Usato dal codice di immissione di testo personalizzato dell'applicazione per inserire il testo nel campo di testo e nell'archivio di backup dei servizi di testo.<br/> |
| [**Interfaccia ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Fornisce il controllo sul pannello input penna di Tablet PC.<br/>                                                                                  |
| [**Interfaccia ITextInputPanelEventSink**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Definisce i metodi che gestiscono gli eventi dell' [**interfaccia ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .<br/>                                      |
| [**Interfaccia ITextInputPanelRunInfo**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Fornisce un metodo per determinare se il pannello di input di testo è attualmente in esecuzione.<br/>                                                      |
| [**Interfaccia ITipAutocompleteClient**](itipautocompleteclient.md)       | Consente al client di chiamare l'oggetto provider di completamento automatico del pannello di input di testo dell'applicazione.<br/>                                      |
| [**Interfaccia ITipAutocompleteProvider**](itipautocompleteprovider.md)   | Gestisce il lato dell'applicazione dell'integrazione di completamento automatico del pannello di input di testo.<br/>                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




