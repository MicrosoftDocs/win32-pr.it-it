---
description: Non è più consigliabile usare le classi C++ WMI che fanno parte del Framework del provider WMI.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Classi di utilità del Framework del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab09c99fe2597cacd81e55a4ed18bd4e286ff16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318551"
---
# <a name="provider-framework-utility-classes"></a>Classi di utilità del Framework del provider

\[Classi C++ WMI che fanno parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori attività di sviluppo, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

Le librerie del Framework del provider Framedyd.dll (versione di debug) e Framedyn.dll (versione finale) implementano diverse classi helper del provider. Alcune funzioni in Framedyn.dll sono state rimosse dai file di intestazione. Per continuare a usare queste funzioni, aggiungere `#define FRAMEWORK_ALLOW_DEPRECATED` al codice prima di includere Fwcommon. h.

È possibile scaricare i singoli provider che non sono più necessari.

Per usare questa funzionalità, è necessario apportare le tre modifiche seguenti al provider in MainDll. cpp:

-   Nella funzione **DllMain** in cui viene chiamato [**CWbemProviderGlue:: FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), è necessario aggiungere un secondo parametro che è un puntatore a un Long.
-   Nella funzione **DllCanUnloadNow** dove si chiama [**CWbemProviderGlue:: FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), è necessario aggiungere un secondo parametro che è un puntatore a Long.
-   Nella funzione **DllGetClassObject** in cui si crea un'istanza di **CWbemGlueFactory** è necessario aggiungere un parametro che è un puntatore a un Long.

In tutti e tre i casi, il puntatore a un oggetto Long deve essere lo stesso puntatore.

> [!Note]  
> In maindll. cpp, le routine **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** e **DllMain** devono essere incapsulate in un blocco try/catch.

 

> [!Caution]  
> Il collegamento delle build di debug del provider con Framedyd. lib per Framedyd.dll. Framedyd.dll si trova nella directory bin di Microsoft Windows Software Development Kit (SDK) \\ che non è inclusa nel percorso di sistema. Quando una build di debug di un provider viene testata con il servizio di gestione Windows, il provider del Framework non verrà caricato perché Framedyd.dll o una delle relative dipendenze non verranno individuate. Pertanto, è necessario copiare Framedyd.dll dalla \\ directory Windows SDK bin alla \\ directory system32 di system32 \\ o aggiungere la directory Windows SDK \\ bin al percorso di ricerca del sistema.

 

Nella tabella seguente sono elencate le classi di utilità del Framework del provider.



| Classe di utilità                                          | Descrizione                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Fornisce funzioni di confronto e manipolazione di stringhe per WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contiene per la creazione e la modifica di matrici di CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Concede l'accesso a una classe contenitore per i puntatori.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Semplifica le conversioni tra diversi formati di runtime del linguaggio C di Windows e ANSI.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contiene funzioni helper utilizzate per calcolare e mantenere la differenza di intervallo di tempo tra due oggetti [**WBEMTime**](wbemtime.md) . |



 

> [!Note]  
> Le classi [**CHString**](chstring.md) e [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) sono simili a Microsoft Foundation Classes (MFC) **CString** e **CStringArray**. Sono disponibili le versioni WMI in modo che gli sviluppatori possano accedere ai metodi di confronto e di manipolazione delle stringhe senza dover accedere a MFC. Anche le classi [**WBEMTime**](wbemtime.md) e [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) sono simili alle classi **CTime** e **CTimeSpan** MFC. Le versioni WMI sono in grado di archiviare tempi di accuratezza nanosecondi e possono anche eseguire la conversione da e verso **BSTR**. Per ulteriori informazioni sulle classi CString, CStringArray, CTime e CTimeSpan, vedere il [Microsoft Foundation Classes](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) su MSDN.

 

I valori **BSTR** restituiti dai metodi [**WBEMTime**](wbemtime.md) sono nel [formato di data e ora](date-and-time-format.md): "ad aaaammgghhmmss. mmmmmmsUUU"

I valori **BSTR** restituiti dai metodi [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) sono in [Formato intervallo](interval-format.md): "ddddddddHHMMSS. mmmmmm: 000"

Sebbene i tempi e gli intervalli di tempo siano archiviati internamente come nanosecondi, non vengono necessariamente archiviati con una precisione di nanosecondi. Ciò è dovuto al fatto che gli oggetti [**WBEMTime**](wbemtime.md) possono essere costruiti utilizzando formati di ora accurati a un secondo (**struct TM** e **time \_ t**). L'aggiunta di posizioni decimali artificiali non aumenta l'accuratezza.

 

 
