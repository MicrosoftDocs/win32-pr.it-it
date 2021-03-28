---
description: Le associazioni di file definiscono il modo in cui la shell considera un tipo di file nel sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Funzionamento delle associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227455"
---
# <a name="how-file-associations-work"></a>Funzionamento delle associazioni di file

Le associazioni di file definiscono il modo in cui la shell considera un [tipo di file](fa-file-types.md) nel sistema.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sulle associazioni di file](#about-file-associations)
-   [Quando è necessario implementare o modificare le associazioni di file](#when-you-should-implement-or-modify-file-associations)
-   [Funzionamento delle associazioni di file](#how-file-associations-work)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-file-associations"></a>Informazioni sulle associazioni di file

Le associazioni di file controllano le funzionalità seguenti:

-   Quale applicazione viene avviata quando un utente fa doppio clic su un file.
-   Quale icona appare per un file per impostazione predefinita.
-   Visualizzazione del tipo di file visualizzato in Esplora risorse.
-   Comandi visualizzati nel menu di scelta rapida di un file.
-   Altre funzionalità dell'interfaccia utente, ad esempio le descrizioni comandi, le informazioni sui riquadri e il riquadro dei dettagli.

Gli sviluppatori di applicazioni possono utilizzare le associazioni di file per controllare il modo in cui la shell considera i tipi di file personalizzati o per associare un'applicazione ai tipi di file esistenti. Ad esempio, quando un'applicazione viene installata, l'applicazione può verificare la presenza di associazioni di file esistenti e creare o eseguire l'override di tali associazioni di file.

Gli utenti possono controllare alcuni aspetti delle associazioni di file per personalizzare il modo in cui la shell considera un tipo di file usando l'interfaccia utente **aperta con** oppure modificando il registro di sistema.

Nella finestra di Esplora risorse visualizzata nella schermata seguente la shell Visualizza icone diverse per ogni file, in base all'icona associata al tipo di file. Se l'utente fa doppio clic sull' **immagine bitmap di esempio** file, la shell avvia Paint e la usa per aprire il file perché in questo sistema, Paint è associato ai file con estensione bmp. Gli utenti possono controllare queste azioni usando le associazioni di file.

![illustrazione di come funzionano le associazioni di file in pratica](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Quando è necessario implementare o modificare le associazioni di file

Le applicazioni possono utilizzare i file per diversi scopi: alcuni file vengono utilizzati esclusivamente dall'applicazione e non sono in genere accessibili dagli utenti, mentre gli altri file vengono creati dall'utente e spesso vengono aperti, cercati e visualizzati dalla Shell.

A meno che il tipo di file personalizzato non venga usato esclusivamente dall'applicazione, è necessario implementare le associazioni di file. Come regola generale, implementare le associazioni di file per il tipo di file personalizzato se si prevede che l'utente interagisca direttamente con questi file in qualsiasi modo. Che include l'uso della Shell per esplorare e aprire i file, cercare il contenuto o le proprietà dei file e visualizzare in anteprima i file.

Se l'applicazione gestisce un tipo di file esistente, non modificare l'associazione file, a meno che non si desideri modificare il modo in cui la shell gestisce tutti i file di questo tipo.

## <a name="how-file-associations-work"></a>Funzionamento delle associazioni di file

I file vengono esposti nella shell come elementi della shell. Per controllare le associazioni di file, gli sviluppatori di applicazioni possono registrare un mapping tra il tipo di file e i gestori (oggetti COM che forniscono funzionalità per gli elementi della shell del tipo di file). Quando la shell deve eseguire una query per le associazioni di file di un tipo di file, crea una matrice di chiavi del registro di sistema contenenti le associazioni per il tipo di file e controlla queste chiavi per le associazioni di file appropriate da usare.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni di base concettuali sulle associazioni di file, vedere [Cenni preliminari su verbi e associazioni di file](fa-verbs.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
</dt> <dt>

[Tipo di file Verifier](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>

 

 



