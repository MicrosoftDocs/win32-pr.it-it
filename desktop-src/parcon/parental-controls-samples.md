---
description: Esempi di controllo genitori
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Esempi di controllo genitori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23111e42b670c30630b7ebd250c94ba2f148fcf4a81874fcc3c360db9b4bbd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971610"
---
# <a name="parental-controls-samples"></a>Esempi di controllo genitori

Il codice di esempio per controllo genitori è disponibile in path <installation directory> \\ Windows Samples \\ <version number> \\ \\ Security \\ ParentControls. Gli esempi sono i seguenti:

## <a name="utilities"></a>Utilità

Funzionalità helper per la gestione COM di base, le operazioni di stringa SID e la funzionalità di lettura e scrittura WMI. Tutti gli altri esempi dipendono da questo progetto, se non diversamente specificato.

## <a name="complianceapi"></a>ComplianceAPI

Applicazione console guidata dalla riga di comando che illustra come usare l'API di conformità per recuperare un subset chiave di impostazioni per un utente.

## <a name="complianceapp"></a>ComplianceApp

Semplice applicazione console che illustra l'uso dell'API di conformità per verificare la registrazione delle restrizioni necessarie e specifiche. Se sono abilitate restrizioni di tempo, l'applicazione attende anche gli eventi di disconnessione imminenti.

## <a name="uiextensibility"></a>Estendibilità dell'interfaccia utente

Applicazione console guidata dalla riga di comando che illustra l'uso delle API WMI e dello schema WPC per elencare, eseguire query, aggiungere, modificare ed eliminare le voci di collegamento di estendibilità dell'interfaccia utente.

Riga di comando di esempio per sample:

"D: \\ WPC \\ Samples Security \\ \\ ParentControls \\ UIExtensibility \\ debug \\ UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentControls/UiExtRC/debug/UiExtRC.dll,-101 /s:s D:/WPC/Samples/Security/ParentControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c: \\ windows \\Notepad.exe

dove UiExtRC è una DLL di risorse semplice con risorse di tipo stringa per id 101 e 103 e 24x24 pixel a 32 bit con bitmap alfa per le risorse 104 e 106.

## <a name="webextensibility"></a>WebExtensibility

Applicazione console guidata dalla riga di comando che illustra come usare le API WMI e lo schema WPC per elencare, aggiungere ed eliminare le voci di esenzione url o applicazione HTTP e per impostare e reimpostare un override del filtro contenuto Web con le proprietà FilterID e FilterName.

L'accesso all'applicazione HTTP di sola lettura e agli elenchi di esenzioni URL non viene visualizzato, ma il codice per leggere gli elenchi è identico a quello per il caso di lettura/scrittura, ad eccezione della modifica del parametro WMI.

 

 



