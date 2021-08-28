---
description: Prima di iniziare a sviluppare un'applicazione Microsoft Windows HTTP Services (WinHTTP), è necessario decidere se usare l'API C/C++ o l'interfaccia COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Scelta di un'interfaccia WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7772959bd76dc7a257abc180c915f99df988a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472357"
---
# <a name="choosing-a-winhttp-interface"></a>Scelta di un'interfaccia WinHTTP

Prima di iniziare a sviluppare un'applicazione Microsoft Windows HTTP Services (WinHTTP), è necessario decidere se usare l'API C/C++ o l'interfaccia COM. La tabella seguente riepiloga i vantaggi e gli svantaggi associati a ognuno di questi approcci.




|  | C/C++ API | Interfaccia COM | 
|--|-----------|---------------|
| Vantaggi | <ul><li>Le risposte possono essere elaborate in blocchi, il che è più efficiente.</li><li>Le operazioni POST possono anche essere elaborate in blocchi, accelerando il tempo di elaborazione.</li><li>Supporto di AutoProxy.</li><li>Accesso al set di funzionalità completo di WinHTTP.</li><li>I dati binari possono essere gestiti facilmente.</li></ul> | <ul><li>La creazione di un'applicazione è semplice e richiede meno righe di codice rispetto all'API C/C++.</li><li>L'interfaccia può essere usata dai linguaggi di scripting.</li></ul> | 
| Svantaggi | <ul><li>L'elaborazione è più complessa.</li><li>L'API C/C++ richiede più passaggi rispetto all'interfaccia COM per eseguire le stesse azioni.</li><li>La configurazione di una richiesta richiede più codice.</li></ul> | <ul><li>L'interfaccia COM non fornisce l'accesso al set di funzionalità completo di WinHTTP.</li><li>È difficile gestire i tipi di dati binari in alcuni linguaggi di scripting, ad esempio VBScript e JScript.</li><li>L'interfaccia COM non supporta AutoProxy.</li><li>Le applicazioni devono usare il modello APARTMENT_THREADED COM.</li><li>Prima di iniziare l'elaborazione di una risposta, è necessario ricevere e memorizzato nel buffer l'intera risposta.</li></ul> | 




 

 

 



