---
description: L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per l'esecuzione di applicazioni e la gestione del sistema operativo.
title: Shell di Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979903"
---
# <a name="windows-shell"></a>Shell di Windows

L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per l'esecuzione di applicazioni e la gestione del sistema operativo. I più numerosi e familiari di questi oggetti sono le cartelle e i file che risiedono in unità disco del computer. Sono inoltre disponibili numerosi oggetti virtuali che consentono all'utente di eseguire attività quali l'invio di file alle stampanti remote o l'accesso al Cestino. La shell organizza questi oggetti in uno spazio dei nomi gerarchico e fornisce a utenti e applicazioni un modo coerente ed efficiente per accedere e gestire gli oggetti.

## <a name="shell-development-scenarios"></a>Scenari di sviluppo della shell

Gli scenari di sviluppo seguenti sono correlati allo sviluppo di applicazioni:

-   Estensione della shell, che consiste nella creazione di un'origine dati (rispetto al modello di dati della Shell)
-   Implementazione di un sottoinsieme delle attività dell'origine dati della shell
-   Librerie di supporto e visualizzazioni di elementi in Esplora risorse
-   Uso della finestra di dialogo file comune
-   Implementazione degli elementi del pannello di controllo
-   Gestione delle notifiche

Gli scenari di sviluppo seguenti si riferiscono alla proprietà del formato di file:

-   Implementazione di un sottoinsieme delle attività dell'origine dati della shell
-   Implementazione di qualsiasi gestore
-   Supporto della ricerca desktop

Gli scenari di sviluppo seguenti si riferiscono alla proprietà dell'archiviazione dei dati:

-   Supporto per la ricerca desktop e OpenSearch
-   Implementazione di un sottoinsieme delle attività dell'origine dati della shell (cartelle virtuali)
-   Librerie di supporto in Esplora risorse

Lo scenario di sviluppo seguente si riferisce al supporto dei dispositivi:

-   Esecuzione automatica e riproduzione automatica

## <a name="windows-shell-sdk-documentation"></a>Documentazione di Windows Shell SDK

Questa documentazione è suddivisa in tre sezioni principali:

-   La [Guida](intro.md) per gli sviluppatori della shell fornisce materiale concettuale sul funzionamento della shell e su come usare l'API della shell nell'applicazione.
-   La sezione di [riferimento della shell](shell-reference-bumper.md) documenta gli elementi di programmazione che costituiscono le varie API della shell.
-   [Esempi di Shell](samples-entry.md) fornisce collegamenti ad esempi di codice correlati.

La tabella seguente fornisce una descrizione della sezione di riferimento della shell. Se non specificato diversamente, tutti gli elementi di programmazione sono documentati in C++ non gestito.



| Sezione                                                               | Descrizione                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Classi shell](classes.md)                                          | In questa sezione vengono descritte le classi della shell di Windows Select.                                                                 |
| [Interfacce della shell](interfaces.md)                                    | In questa sezione vengono descritte le interfacce di Windows Shell Component Object Model (COM).                                    |
| [Funzioni della shell](functions.md)                                      | In questa sezione vengono descritte le funzioni della shell di Windows.                                                                  |
| [Funzioni di callback della shell](callbacks.md)                             | In questa sezione vengono descritti i modelli di funzioni di callback della shell di Windows.                                               |
| [Costanti, enumerazioni e flag della shell](consts-enums-flags.md)    | In questa sezione vengono descritte le costanti, le enumerazioni e i flag della shell di Windows utilizzati nelle API della shell.                  |
| [Funzioni di utilità Lightweight Shell](shlwapi.md)                    | In questa sezione vengono descritte le funzioni di utilità Lightweight per la shell di Windows fornite in Shlwapi.dll.                      |
| [Macro della shell](macros.md)                                            | In questa sezione vengono descritte le macro di utilità della shell di Windows.                                                             |
| [Messaggi e notifiche della shell](messages.md)                      | In questa sezione vengono descritti i messaggi e le notifiche inviati dagli elementi della shell di Windows.                         |
| [Oggetti Shell per gli script e Microsoft Visual Basic](objects.md) | In questa sezione vengono descritti gli oggetti di Windows implementati dalla Shell per l'utilizzo nello scripting e in Microsoft Visual Basic. |
| [Oggetti Shell per C++](objects-cpp.md)                              | In questa sezione vengono descritti gli oggetti Windows C++ implementati dalla Shell.                                             |
| [Schemi della shell](schemas.md)                                          | In questa sezione vengono descritti gli schemi del manifesto della libreria, della proprietà e del trasferimento utilizzati dalla shell di Windows.                   |
| [Strutture della shell](structures.md)                                    | In questa sezione vengono descritte le strutture della shell di Windows utilizzate nelle API della shell.                                          |



 

 

 



