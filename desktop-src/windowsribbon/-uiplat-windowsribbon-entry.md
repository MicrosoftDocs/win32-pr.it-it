---
title: Framework della barra multifunzione di Windows
description: Leggere un'introduzione al framework della barra multifunzione di Windows, un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Barra multifunzione di Windows
- Barra multifunzione
- Documentazione della barra multifunzione di Windows
- Documentazione della barra multifunzione
- API della barra multifunzione di Windows
- API della barra multifunzione
- Barra multifunzione di Windows, framework
- Barra multifunzione, framework
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
- barra multifunzione, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211e1e1cf39a547ad0edbc0c180c62e2f40e15fa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406364"
---
# <a name="windows-ribbon-framework"></a>Framework della barra multifunzione di Windows

Il framework della barra multifunzione di Windows è un sistema di presentazione dei comandi ricco che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali. Analogamente alle funzionalità e all'aspetto dell'interfaccia utente Fluent di Microsoft Office 2007, il framework della barra multifunzione è costituito da una barra dei comandi della barra multifunzione che espone le funzionalità principali di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione e un sistema di menu di scelta rapida.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                           | Descrizione                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cenni preliminari sul framework della barra multifunzione](windowsribbon-overviews-entry.md)<br/>      | Negli argomenti contenuti in questa sezione vengono esaminati i concetti fondamentali del framework della barra multifunzione. <br/>                                                                                                                   |
| [Guide per gli sviluppatori del framework della barra multifunzione](windowsribbon-guides-entry.md)<br/>  | Gli argomenti contenuti in questa sezione descrivono aspetti specifici del framework della barra multifunzione di Windows. <br/>                                                                                                          |
| [Libreria di controlli del framework della barra multifunzione](windowsribbon-controls-entry.md)<br/> | Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione. I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espongono la funzionalità Command.<br/> |
| [Informazioni di riferimento sul framework della barra multifunzione](windowsribbon-reference-entry.md)<br/>      | Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per il framework della barra multifunzione.<br/>                                                                                                       |
| [Esempi di framework della barra multifunzione](windowsribbon-samples-entry.md)<br/>          | Gli argomenti contenuti in questa sezione forniscono informazioni dettagliate sugli esempi di codice che supportano la documentazione del framework della barra multifunzione di Windows. <br/>                                                                     |
| [Glossario del framework della barra multifunzione](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Sviluppatori

Il framework della barra multifunzione di Windows è progettato per l'uso da parte di sviluppatori e finestre di progettazione dell'interfaccia utente di C/C++.

Competenze consigliate:

-   Programmazione COM
-   Programmazione api Windows
-   Programmazione XML/XAML

Conoscenze di base consigliate:

-   Concetti relativi alla programmazione dell'interfaccia utente
-   Concetti generali dell'interfaccia utente

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato               | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e aggiornamento [della piattaforma per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato               | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e [aggiornamento della piattaforma per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| File di intestazione e IDL                   | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione di Windows sia per Windows Vista che per Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows [Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) possono Windows Update se è installato l'aggiornamento richiesto; In caso contrario, Windows Update scaricarlo e installarlo in background.

 

## <a name="see-also"></a>Vedere anche

[Component Object Model (COM)](../com/component-object-model--com--portal.md)


[API Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

