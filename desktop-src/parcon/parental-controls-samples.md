---
description: Esempi di controlli padre
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Esempi di controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316432"
---
# <a name="parental-controls-samples"></a>Esempi di controlli padre

Il codice di esempio per i controlli padre è disponibile in percorso <installation directory> \\ Windows \\ <version number> \\ Samples \\ Security \\ parentalcontrols. Gli esempi sono i seguenti:

## <a name="utilities"></a>Utilità

Funzionalità di supporto per la gestione COM di base, le operazioni sulle stringhe SID e la funzionalità di lettura e scrittura WMI. Tutti gli altri esempi dipendono da questo progetto se non diversamente specificato.

## <a name="complianceapi"></a>ComplianceAPI

Applicazione console guidata dalla riga di comando che illustra come usare l'API di conformità per recuperare un sottoinsieme di impostazioni chiave per un utente.

## <a name="complianceapp"></a>ComplianceApp

Semplice applicazione console che illustra l'uso dell'API di conformità per verificare la registrazione richiesta e restrizioni specifiche. Se sono abilitate le restrizioni temporali, l'applicazione attende anche gli eventi di disconnessione imminenti.

## <a name="uiextensibility"></a>UIExtensibility

Applicazione console guidata dalla riga di comando che illustra l'uso delle API WMI e dello schema WPC per elencare, eseguire query, aggiungere, modificare ed eliminare voci di collegamento di estensibilità dell'interfaccia utente.

Esempio di riga di comando per esempio:

"D: \\ WPC \\ Samples \\ Security \\ parentalcontrols \\ UIExtensibility \\ debug \\ UIExtensibility" Add/g: {FD59BB7F-54AB-11dB-9666-00E08161165F}/c: 0/N: D:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll-101/S: d:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll,-103/I: d:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll,-104/D: D:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe

dove UiExtRC è una DLL di risorse semplice con risorse di stringa per l'ID 101 e 103 e 24x24 pixel 32 bit con bitmap Alpha per le risorse 104 e 106.

## <a name="webextensibility"></a>Estendibilità

Applicazione console guidata dalla riga di comando che illustra come usare le API WMI e lo schema WPC per elencare, aggiungere ed eliminare le voci di esenzione URL o applicazione HTTP e per impostare e reimpostare l'override di un filtro contenuto Web con le proprietà FilterID e FilterName.

L'accesso all'applicazione HTTP di sola lettura e agli elenchi di esenzione URL non viene visualizzato, ma il codice per leggere gli elenchi è identico a quello per il caso di lettura/scrittura, fatta eccezione per la modifica del parametro WMI.

 

 



