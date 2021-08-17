---
description: Le classi WMI C++ che fanno parte di WMI Provider Framework non sono più consigliate per l'uso.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Classi di utilità del framework del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254a1321ab835c86e7b4bf0e5cb14048be0352290707a61aaf993a9a6cc6e8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130983"
---
# <a name="provider-framework-utility-classes"></a>Classi di utilità del framework del provider

\[Classi WMI C++ che fanno parte di WMI Provider Framework che è ora considerato in stato finale e non saranno disponibili ulteriori sviluppo, miglioramenti o aggiornamenti per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Le librerie del framework Framedyd.dll provider (versione di debug) e Framedyn.dll (versione di rilascio) implementano diverse classi helper del provider. Alcune funzioni in Framedyn.dll sono state rimosse dai file di intestazione. Per continuare a usare queste funzioni, aggiungere `#define FRAMEWORK_ALLOW_DEPRECATED` al codice prima di includere Fwcommon.h.

È possibile scaricare singoli provider che non sono più necessari.

Per usare questa funzionalità, è necessario apportare le tre modifiche seguenti al provider in MainDll.cpp:

-   Nella funzione **DllMain** in cui si chiama [**CWbemProviderGlue::FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))è necessario aggiungere un secondo parametro che è un puntatore a un long.
-   Nella funzione **DllCanUnloadNow** in cui si chiama [**CWbemProviderGlue::FrameworkLogoffDLL,**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))è necessario aggiungere un secondo parametro che è un puntatore a un long.
-   Nella funzione **DllGetClassObject in** cui si crea un'istanza di **CWbemGlueFactory** è necessario aggiungere un parametro che è un puntatore a un long.

In tutti e tre i casi, il puntatore a un oggetto long deve essere lo stesso puntatore.

> [!Note]  
> In Maindll.cpp è necessario eseguire il wrapping delle routine **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** e **DllMain** in un blocco try/catch.

 

> [!Caution]  
> Le build di debug del provider si collegano a Framedyd.lib per Framedyd.dll. Framedyd.dll si trova nella directory bin di Microsoft Windows Software Development Kit (SDK) che \\ non è inclusa nel percorso di sistema. Quando una build di debug di un provider viene testata con il servizio di gestione di Windows, il caricamento del provider di framework non riesce perché Framedyd.dll o una delle relative dipendenze non verrà individuata. Pertanto, è necessario copiare Framedyd.dll dalla directory bin di Windows SDK alla \\ \\ directory system32 \\ wbem oppure aggiungere la directory bin di Windows SDK al percorso di ricerca \\ del sistema.

 

Nella tabella seguente sono elencate le classi di utilità del framework del provider.



| Classe di utilità                                          | Descrizione                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Fornisce funzioni di confronto e manipolazione di stringhe per WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contiene per la creazione e la modifica di matrici di CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Concede l'accesso a una classe contenitore per i puntatori.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Facilita le conversioni tra i vari Windows e i formati di run-time C ANSI.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contiene funzioni helper usate per calcolare e mantenere la differenza di intervallo di tempo tra due [**oggetti WBEMTime.**](wbemtime.md) |



 

> [!Note]  
> Le [**classi CHString**](chstring.md) [**e CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) sono simili alle classi Microsoft Foundation Classes (MFC) **CString** e **CStringArray**. Le versioni WMI sono disponibili in modo che gli sviluppatori possano accedere ai metodi di confronto e modifica delle stringhe senza dover accedere a MFC. Anche [**le classi WBEMTime**](wbemtime.md) [**e WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) sono simili alle classi **CTime** e **CTimeSpan** MFC. Le versioni WMI sono in grado di archiviare l'accuratezza da tempo a nanosecondo e possono anche eseguire la conversione da e verso **BSTR.** Per altre informazioni sulle classi CString, CStringArray, CTime e CTimeSpan, [vedere](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) il Microsoft Foundation Classes su MSDN.

 

**I valori BSTR** restituiti dai [**metodi WBEMTime**](wbemtime.md) sono [in](date-and-time-format.md)formato data e ora: "aaaammggHHMMSS.mmmmmmsUUU"

**I valori BSTR** restituiti [**dai metodi WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) sono in formato [intervallo:](interval-format.md)"dddddddddHHMMSS.mmmmmm:000"

Anche se gli intervalli di tempo e di tempo vengono archiviati internamente come nanosecondi, non vengono necessariamente archiviati con accuratezza nanosecondo. Questo perché [**gli oggetti WBEMTime**](wbemtime.md) possono essere costruiti usando formati di ora accurati a un secondo (**struct tm** e **time \_ t**). L'aggiunta di posizioni decimali artificiali non aumenta l'accuratezza.

 

 
