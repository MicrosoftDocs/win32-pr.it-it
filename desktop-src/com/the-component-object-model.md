---
title: Component Object Model (COM)
description: Component Object Model (COM)
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708038"
---
# <a name="the-component-object-model"></a>Component Object Model (COM)

Microsoft Component Object Model (COM) è un sistema indipendente dalla piattaforma, distribuito e orientato a oggetti per la creazione di componenti software binari in grado di interagire. COM è la tecnologia di base per Microsoft OLE (documenti composti), ActiveX (componenti abilitati per Internet) e altri.

Per comprendere COM (e pertanto tutte le tecnologie basate su COM), è fondamentale comprendere che non si tratta di un linguaggio orientato a oggetti, ma di uno standard. Né COM specificano la struttura di un'applicazione; la lingua, la struttura e i dettagli di implementazione vengono lasciati allo sviluppatore di applicazioni. COM specifica invece un modello a oggetti e requisiti di programmazione che consentono agli oggetti COM (detti anche componenti COM o semplicemente a *oggetti*) di interagire con altri oggetti. Questi oggetti possono trovarsi all'interno di un singolo processo, in altri processi, e possono anche trovarsi su computer remoti. Possono essere scritti in linguaggi diversi e possono essere strutturalmente molto diversi, motivo per cui COM viene definito *standard binario*. standard applicato dopo che un programma è stato convertito in codice macchina binario.

L'unico requisito per il linguaggio COM è che il codice viene generato in un linguaggio in grado di creare strutture di puntatori e, in modo esplicito o implicito, chiamare funzioni tramite puntatori. I linguaggi orientati a oggetti, ad esempio C++ e Smalltalk, forniscono meccanismi di programmazione che semplificano l'implementazione di oggetti COM, ma è possibile utilizzare linguaggi quali C, Java e VBScript per creare e utilizzare oggetti COM.

COM definisce la natura essenziale di un oggetto COM. In generale, un oggetto software è costituito da un set di dati e dalle funzioni che modificano i dati. Un oggetto COM è un oggetto in cui l'accesso ai dati di un oggetto viene effettuato esclusivamente tramite uno o più set di funzioni correlate. Questi set di funzioni sono denominati *interfacce* e le funzioni di un'interfaccia sono denominate *Metodi*. COM richiede inoltre che l'unico modo per accedere ai metodi di un'interfaccia sia tramite un puntatore all'interfaccia.

Oltre a specificare lo standard dell'oggetto binario di base, COM definisce alcune interfacce di base che forniscono funzioni comuni a tutte le tecnologie basate su COM e fornisce un numero ridotto di funzioni richieste da tutti i componenti. COM definisce anche il modo in cui gli oggetti interagiscono in un ambiente distribuito e ha aggiunto funzionalità di sicurezza che consentono di garantire l'integrità del sistema e dei componenti.

Negli argomenti seguenti di questa sezione vengono descritti i problemi COM di base relativi alla progettazione di oggetti COM:

-   [Oggetti e interfacce COM](com-objects-and-interfaces.md)
-   [Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
-   [Riutilizzo di oggetti](reusing-objects.md)
-   [Libreria COM](the-com-library.md)
-   [Gestione dell'allocazione di memoria](managing-memory-allocation.md)

 

 




