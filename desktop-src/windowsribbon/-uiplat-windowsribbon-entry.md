---
title: Windows Framework della barra multifunzione
description: Leggere un'introduzione al framework Windows ribbon, un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows Nastro
- Barra multifunzione
- Windows Documentazione della barra multifunzione
- Documentazione della barra multifunzione
- Windows API della barra multifunzione
- API della barra multifunzione
- Windows Barra multifunzione, framework
- Barra multifunzione, framework
- Windows Barra multifunzione, informazioni su
- Barra multifunzione, informazioni su
- Windows Barra multifunzione, componenti
- Barra multifunzione, componenti
- Windows Barra multifunzione, visualizzazioni
- Barra multifunzione, visualizzazioni
- Windows Barra multifunzione, architettura
- Barra multifunzione, architettura
- Windows Barra multifunzione, API
- Barra multifunzione, API
- Windows Barra multifunzione, sicurezza
- Barra multifunzione, sicurezza
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 98f7dbf42d604f93c76bb9897aa25918d45d126f
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691650"
---
# <a name="windows-ribbon-framework"></a>Windows Framework della barra multifunzione

Il framework Windows della barra multifunzione è un sistema di presentazione dei comandi ricco che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali. Analogamente alle funzionalità e all'aspetto dell'interfaccia utente di Microsoft Office 2007 Fluent, il framework della barra multifunzione è costituito da una barra dei comandi della barra multifunzione che espone le principali funzionalità di un'applicazione tramite una serie di schede nella parte superiore di una finestra dell'applicazione e un sistema di menu di scelta rapida.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                           | Descrizione                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cenni preliminari sul framework della barra multifunzione](windowsribbon-overviews-entry.md)<br/>      | Negli argomenti contenuti in questa sezione vengono esaminati i concetti fondamentali del framework della barra multifunzione. <br/>                                                                                                                   |
| [Guide per gli sviluppatori di Ribbon Framework](windowsribbon-guides-entry.md)<br/>  | Gli argomenti contenuti in questa sezione descrivono aspetti specifici del framework Windows ribbon. <br/>                                                                                                          |
| [Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)<br/> | Negli argomenti contenuti in questa sezione viene descritto il set di controlli inclusi nel framework della barra multifunzione. I controlli elencati di seguito sono gli oggetti dell'interfaccia utente in una barra multifunzione che espongono la funzionalità Command.<br/> |
| [Informazioni di riferimento sul framework della barra multifunzione](windowsribbon-reference-entry.md)<br/>      | Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per il framework della barra multifunzione.<br/>                                                                                                       |
| [Esempi di framework della barra multifunzione](windowsribbon-samples-entry.md)<br/>          | Gli argomenti contenuti in questa sezione forniscono informazioni dettagliate sugli esempi di codice che supportano la documentazione Windows del framework della barra multifunzione. <br/>                                                                     |
| [Glossario di Ribbon Framework](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Sviluppatori

Il Windows della barra multifunzione è progettato per l'uso da parte di sviluppatori e finestre di progettazione dell'interfaccia utente C/C++.

Competenze consigliate:

- Programmazione COM
- Windows Programmazione api
- Programmazione XML/XAML

Conoscenze di base consigliate:

- Concetti di programmazione dell'interfaccia utente
- Concetti generali dell'interfaccia utente

## <a name="minimum-requirements"></a>Requisiti minimi



| Requisito | Valore |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato               | Windows 7<br/> Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Server minimo supportato               | Windows Server 2008 R2<br/> Windows Server 2008 con SP2 e aggiornamento della piattaforma [per Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| File di intestazione e IDL                   | uiribbon.h, uiribbon.idl                                                                                                                                                 |



 

> [!Note]  
> L'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) e l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) sono set di librerie di runtime che consentono agli sviluppatori di scegliere come destinazione le applicazioni della barra multifunzione Windows Windows Vista e Windows Server 2008. Gli aggiornamenti della piattaforma saranno disponibili per tutti i Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma [per Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) o l'aggiornamento della piattaforma per Windows Server [2008](https://msdn.microsoft.com/library/dd378748.aspx) possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, l Windows Update lo scariderà e lo installerà in background.

 

## <a name="see-also"></a>Vedere anche

[Component Object Model (COM)](../com/component-object-model--com--portal.md)


[API Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

