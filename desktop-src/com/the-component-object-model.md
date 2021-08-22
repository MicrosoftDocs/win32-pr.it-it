---
title: Component Object Model (COM)
description: Component Object Model (COM)
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad81adeaf41670468dd41bbf344a3fd7358c14f4b3cbeb2e482812a083ecfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462341"
---
# <a name="the-component-object-model"></a>Component Object Model (COM)

Microsoft Component Object Model (COM) è un sistema orientato a oggetti, distribuito e indipendente dalla piattaforma per la creazione di componenti software binari in grado di interagire. COM è la tecnologia di base per OLE di Microsoft (documenti composti), ActiveX (componenti abilitati per Internet) e altri.

Per comprendere COM (e quindi tutte le tecnologie basate su COM), è fondamentale comprendere che non si tratta di un linguaggio orientato a oggetti, ma di uno standard. Né COM specifica come deve essere strutturata un'applicazione; I dettagli relativi al linguaggio, alla struttura e all'implementazione vengono lasciati allo sviluppatore dell'applicazione. COM specifica invece un modello a oggetti e i requisiti di programmazione che consentono agli oggetti COM (denominati anche componenti COM o talvolta semplicemente oggetti *)* di interagire con altri oggetti. Questi oggetti possono essere all'interno di un singolo processo, in altri processi e possono anche essere in computer remoti. Possono essere scritti in linguaggi diversi e strutturalmente piuttosto diversi, motivo per cui COM viene definito *standard binario.* uno standard che si applica dopo la traduzione di un programma in codice macchina binario.

L'unico requisito del linguaggio per COM è che il codice venga generato in un linguaggio in grado di creare strutture di puntatori e, in modo esplicito o implicito, chiamare funzioni tramite puntatori. I linguaggi orientati a oggetti come C++ e Smalltalk forniscono meccanismi di programmazione che semplificano l'implementazione di oggetti COM, ma linguaggi come C, Java e VBScript possono essere usati per creare e usare oggetti COM.

COM definisce la natura essenziale di un oggetto COM. In generale, un oggetto software è costituito da un set di dati e da funzioni che modificano i dati. Un oggetto COM è un oggetto in cui l'accesso ai dati di un oggetto viene ottenuto esclusivamente tramite uno o più set di funzioni correlate. Questi set di funzioni sono denominati *interfacce* e le funzioni di un'interfaccia sono denominate *metodi*. COM richiede inoltre che l'unico modo per accedere ai metodi di un'interfaccia sia tramite un puntatore all'interfaccia .

Oltre a specificare lo standard degli oggetti binari di base, COM definisce alcune interfacce di base che forniscono funzioni comuni a tutte le tecnologie basate su COM e fornisce un numero ridotto di funzioni richieste da tutti i componenti. COM definisce anche il modo in cui gli oggetti funzionano insieme in un ambiente distribuito e ha aggiunto funzionalità di sicurezza che consentono di garantire l'integrità del sistema e dei componenti.

Negli argomenti seguenti di questa sezione vengono descritti i problemi COM di base relativi alla progettazione di oggetti COM:

-   [Interfacce e oggetti COM](com-objects-and-interfaces.md)
-   [Uso e implementazione di IUnknown](using-and-implementing-iunknown.md)
-   [Riutilizzo di oggetti](reusing-objects.md)
-   [Libreria COM](the-com-library.md)
-   [Gestione dell'allocazione di memoria](managing-memory-allocation.md)

 

 




