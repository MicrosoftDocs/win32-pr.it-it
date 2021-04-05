---
description: Poiché lo script di installazione può essere eseguito all'esterno della sessione di installazione in cui è stato scritto, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione.
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: Recupero delle informazioni di contesto per le azioni personalizzate di esecuzione posticipata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cd956509a5b8a4c92e0a53bfa455154a59bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753514"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>Recupero delle informazioni di contesto per le azioni personalizzate di esecuzione posticipata

Poiché lo script di installazione può essere eseguito all'esterno della sessione di installazione in cui è stato scritto, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione. In questo caso, le proprietà e l'handle di sessione originali impostati durante la sequenza di installazione non sono disponibili per un'azione personalizzata di esecuzione posticipata. Tutte le funzioni che richiedono un handle di sessione sono limitate ad alcuni metodi che possono recuperare informazioni sul contesto oppure le proprietà necessarie durante l'esecuzione dello script devono essere scritte nello script di installazione. Ad esempio, le azioni personalizzate posticipate che chiamano librerie a collegamento dinamico (dll) passano un handle che può essere utilizzato solo per ottenere una quantità molto limitata di informazioni. È possibile accedere alle funzioni che non richiedono un handle di sessione da un'azione personalizzata posticipata.

Le azioni personalizzate di esecuzione posticipata sono limitate alla chiamata solo delle funzioni seguenti che richiedono un handle.



| Funzione                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | Supporta un set limitato di proprietà se utilizzato con [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md): la proprietà CustomActionData, la proprietà [**ProductCode**](productcode.md) e la proprietà [**UserSID**](usersid.md) . Le [azioni personalizzate di commit](commit-custom-actions.md) non possono usare la funzione [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) per ottenere la proprietà [**ProductCode**](productcode.md) . Le azioni personalizzate di commit possono utilizzare la proprietà CustomActionData per ottenere il codice del prodotto.<br/> |
| [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | Supporta un set limitato di proprietà quando viene usato con [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md): le proprietà CustomActionData e ProductCode.                                                                                                                                                                                                                                                                                                                                                      |
| [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | Quando viene chiamato da [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md), [commit di azioni personalizzate](commit-custom-actions.md)o azioni personalizzate di [rollback](rollback-custom-actions.md), [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) restituisce true o false quando viene richiesto di controllare i parametri della modalità MSIRUNMODE \_ pianificato, MSIRUNMODE \_ commit o MSIRUNMODE \_ rollback. Le richieste di controllo di qualsiasi altro parametro della modalità di esecuzione da un'azione personalizzata posticipata, di commit o di rollback restituiscono false.<br/>                       |
| [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | ID della lingua numerica per il prodotto corrente. Le [azioni personalizzate di commit](commit-custom-actions.md) non possono usare la funzione [**MsiGetLanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) . Le azioni personalizzate di commit possono utilizzare la proprietà CustomActionData per ottenere l'ID della lingua numerica.<br/>                                                                                                                                                                                                                                                           |
| [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | Elabora i messaggi di errore o di stato dall'azione personalizzata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Un'azione personalizzata scritta in JScript o VBScript richiede l'oggetto [**sessione**](session-object.md) di installazione. Si tratta dell' **oggetto Session** del tipo e il programma di installazione lo connette allo script con il nome "Session". Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà seguenti dell'oggetto **Session** per recuperare il contesto.



| Nome                                                           | Descrizione                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Mode (proprietà)**](session-mode.md)                          | Restituisce true per MSIRUNMODE \_ solo pianificato.                                                                                       |
| [**Proprietà Property (oggetto Session)**](session-session.md)  | Restituisce la proprietà CustomActionData, la proprietà [**ProductCode**](productcode.md) o la proprietà [**UserSID**](usersid.md) .        |
| [**Proprietà Language (oggetto Session)**](session-language.md) | Restituisce l'ID della lingua numerica della sessione di installazione.                                                                           |
| [**Message (metodo)**](session-message.md)                      | Chiamato per gestire gli errori e lo stato di avanzamento.                                                                                              |
| [**Proprietà Installer**](session-installer.md)                | Restituisce l'oggetto padre, utilizzato per le funzioni non di sessione, ad esempio l'accesso al registro di sistema e la gestione della configurazione del programma di installazione. |



 

I valori delle proprietà impostati al momento dell'elaborazione della sequenza di installazione nello script potrebbero non essere disponibili al momento dell'esecuzione dello script. Solo il set limitato di proprietà seguente è sempre accessibile per le azioni personalizzate durante l'esecuzione dello script.



| Nome proprietà                      | Descrizione                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CustomActionData                   | Il valore in fase di azione personalizzata viene elaborato nella tabella di sequenza. La proprietà CustomActionData è disponibile solo per le azioni personalizzate di esecuzione posticipata. Le azioni personalizzate immediate non hanno accesso a questa proprietà. |
| [**ProductCode**](productcode.md) | Codice univoco per il prodotto, una stringa [GUID](guid.md) .                                                                                                                                                         |
| [**UserSID**](usersid.md)         | Impostato dal programma di installazione sull'ID di sicurezza (SID) dell'utente.                                                                                                                                                   |



 

Se gli altri dati della proprietà sono necessari per l'azione personalizzata esecuzione posticipata, i relativi valori devono essere archiviati nello script di installazione. Questa operazione può essere eseguita usando una seconda azione personalizzata.

**Per scrivere il valore di una proprietà nello script di installazione per l'utilizzo durante un'azione personalizzata di esecuzione posticipata**

1.  Inserire una piccola azione personalizzata nella sequenza di installazione che imposta la proprietà di interesse su una proprietà con lo stesso nome dell'azione personalizzata esecuzione posticipata. Se, ad esempio, la chiave primaria per l'azione personalizzata esecuzione posticipata è "azione", impostare una proprietà denominata "azione" sulla proprietà X che è necessario recuperare. È necessario impostare la proprietà "azione" nella sequenza di installazione prima dell'azione personalizzata "azione". Sebbene qualsiasi tipo di azione personalizzata possa impostare i dati di contesto, il metodo più semplice consiste nell'usare un'azione personalizzata assegnazione proprietà (ad esempio, [tipo di azione personalizzata 51](custom-action-type-51.md)).
2.  Nel momento in cui viene elaborata la sequenza di installazione, il programma di installazione scriverà il valore della proprietà X nello script di esecuzione come valore della proprietà CustomActionData.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> <dt>

[Riferimento alla proprietà](property-reference.md)
</dt> </dl>

 

 




