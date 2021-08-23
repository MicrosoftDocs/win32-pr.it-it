---
description: Le associazioni di file definiscono il modo in cui la shell considera un tipo di file nel sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Funzionamento delle associazioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd12386ec7e850d160a6377ddff9b807e6dccfe101ad45285bdc9d7f2661a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032729"
---
# <a name="how-file-associations-work"></a>Funzionamento delle associazioni di file

Le associazioni di file definiscono il modo in cui la shell considera [un tipo](fa-file-types.md) di file nel sistema.

Questo argomento è organizzato come segue:

-   [Informazioni sulle associazioni di file](#about-file-associations)
-   [Quando implementare o modificare le associazioni di file](#when-you-should-implement-or-modify-file-associations)
-   [Funzionamento delle associazioni di file](#how-file-associations-work)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-file-associations"></a>Informazioni sulle associazioni di file

Le associazioni di file controllano le funzionalità seguenti:

-   Quale applicazione viene avviata quando un utente fa doppio clic su un file.
-   Icona visualizzata per un file per impostazione predefinita.
-   Visualizzazione del tipo di file in Windows Explorer.
-   Comandi visualizzati nel menu di scelta rapida di un file.
-   Altre funzionalità dell'interfaccia utente, ad esempio descrizioni comando, informazioni sul riquadro e riquadro dei dettagli.

Gli sviluppatori di applicazioni possono usare le associazioni di file per controllare il modo in cui la shell tratta i tipi di file personalizzati o per associare un'applicazione ai tipi di file esistenti. Ad esempio, quando viene installata un'applicazione, l'applicazione può verificare la presenza di associazioni di file esistenti e creare o eseguire l'override di tali associazioni di file.

Gli utenti possono controllare alcuni aspetti delle associazioni di file per personalizzare il modo in cui la shell tratta un tipo di file usando l'interfaccia utente **Apri** con o modificando il Registro di sistema.

Nella finestra Windows Explorer visualizzata nello screenshot seguente, la shell visualizza icone diverse per ogni file, in base all'icona associata al tipo di file. Se l'utente fa doppio clic sul file **Immagine** bitmap di esempio , la shell avvia Paint e lo usa per aprire il file perché in questo sistema, Paint è associato .bmp file. Gli utenti possono controllare queste azioni usando le associazioni di file.

![illustrazione del funzionamento pratico delle associazioni di file](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Quando implementare o modificare le associazioni di file

Le applicazioni possono usare i file per vari scopi: alcuni file vengono usati esclusivamente dall'applicazione e in genere non sono accessibili dagli utenti, mentre altri file vengono creati dall'utente e vengono spesso aperti, cercati e visualizzati dalla shell.

A meno che il tipo di file personalizzato non venga usato esclusivamente dall'applicazione, è necessario implementare le associazioni di file per l'applicazione. Come regola generale, implementare le associazioni di file per il tipo di file personalizzato se si prevede che l'utente interagisca direttamente con questi file in qualsiasi modo. Ciò include l'uso della shell per esplorare e aprire i file, la ricerca del contenuto o delle proprietà dei file e la visualizzazione in anteprima dei file.

Se l'applicazione gestisce un tipo di file esistente, non modificare l'associazione di file a meno che non si voglia modificare il modo in cui la shell gestisce tutti i file di questo tipo.

## <a name="how-file-associations-work"></a>Funzionamento delle associazioni di file

I file vengono esposti nella shell come elementi della shell. Per controllare le associazioni di file, gli sviluppatori di applicazioni possono registrare un mapping tra il tipo di file e i gestori (oggetti COM che forniscono funzionalità per gli elementi della shell del tipo di file). Quando la shell deve eseguire una query per le associazioni di file di un tipo di file, crea una matrice di chiavi del Registro di sistema contenente le associazioni per il tipo di file e controlla le chiavi per le associazioni di file appropriate da usare.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni concettuali sulle associazioni di file, vedere [Panoramica dei verbi e delle associazioni di file.](fa-verbs.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Visualizzazione contenuto per tipo o tipo di file](prophand-content-view.md)
</dt> <dt>

[Verifica del tipo di file](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazioni](fa-associationarray.md)
</dt> </dl>

 

 



