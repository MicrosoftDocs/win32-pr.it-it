---
title: Framework della barra multifunzione di Windows
description: Windows Ribbon Framework è un sofisticato sistema di presentazione dei comandi che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Barra multifunzione di Windows
- Barra multifunzione
- Documentazione della barra multifunzione di Windows
- Documentazione della barra multifunzione
- API della barra multifunzione di Windows
- API Ribbon
- Barra multifunzione di Windows, Framework
- Barra multifunzione, Framework
- Barra multifunzione di Windows, informazioni
- Barra multifunzione, informazioni
- Barra multifunzione di Windows, componenti
- Barra multifunzione, componenti
- Barra multifunzione di Windows, visualizzazioni
- Barra multifunzione, visualizzazioni
- Barra multifunzione di Windows, architettura
- Barra multifunzione, architettura
- Barra multifunzione di Windows, API
- Barra multifunzione, API
- Barra multifunzione di Windows, sicurezza
- Barra multifunzione, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6906401573cb244ddc4386faf8c283d7938a0ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964067"
---
# <a name="windows-ribbon-framework"></a>Framework della barra multifunzione di Windows

Windows Ribbon Framework è un sofisticato sistema di presentazione dei comandi che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali. Analogamente alla funzionalità e all'aspetto dell'interfaccia utente di Microsoft Office 2007 Fluent, il Framework della barra multifunzione è costituito da una barra dei comandi della barra multifunzione che espone le funzionalità principali di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione e un sistema di menu di scelta rapida.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                           | Descrizione                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramiche sul Framework della barra multifunzione](windowsribbon-overviews-entry.md)<br/>      | Negli argomenti contenuti in questa sezione vengono illustrati i concetti di base del Framework della barra multifunzione. <br/>                                                                                                                   |
| [Guide per gli sviluppatori del Framework Ribbon](windowsribbon-guides-entry.md)<br/>  | Gli argomenti contenuti in questa sezione descrivono aspetti specifici del Framework della barra multifunzione di Windows. <br/>                                                                                                          |
| [Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)<br/> | Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione. I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espone la funzionalità del comando.<br/> |
| [Informazioni di riferimento sul Framework Ribbon](windowsribbon-reference-entry.md)<br/>      | Negli argomenti contenuti in questa sezione vengono fornite le specifiche di riferimento per il Framework della barra multifunzione.<br/>                                                                                                       |
| [Esempi di Framework della barra multifunzione](windowsribbon-samples-entry.md)<br/>          | Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione del Framework della barra multifunzione di Windows. <br/>                                                                     |
| [Glossario del Framework della barra multifunzione](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Sviluppatori

Il Framework della barra multifunzione di Windows è progettato per essere utilizzato dagli sviluppatori C/C++ e dalle finestre di progettazione dell'interfaccia utente

Proficiencies consigliata:

-   Programmazione COM
-   Programmazione API Windows
-   Programmazione XML/XAML

Conoscenza fondamentale consigliata:

-   Concetti relativi alla programmazione dell'interfaccia utente
-   Concetti generali dell'interfaccia utente

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato               | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato               | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| File di intestazione e IDL                   | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> L' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di utilizzare applicazioni della barra multifunzione di Windows in Windows vista e Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l' [aggiornamento della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l' [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.

 

## <a name="see-also"></a>Vedere anche

[Component Object Model (COM)](../com/component-object-model--com--portal.md)


[API Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

