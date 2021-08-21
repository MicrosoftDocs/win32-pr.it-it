---
title: Interfacce ADSI
description: Questo argomento descrive le categorie usate per le interfacce ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- Interfacce ADSI ADSI
- ADSI ADSI , riferimento, interfacce
- interfacce ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75463a2b9ce70013482d2abee4f21ff786e7914cff0fefe691c562c4f39edb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023819"
---
# <a name="adsi-interfaces"></a>Interfacce ADSI

Active Directory Service Interfaces (ADSI) supporta un set ricco di interfacce che possono essere classificate in base alle categorie seguenti:

-   [Core](core-interfaces.md). Queste interfacce forniscono le funzioni di gestione degli oggetti di base degli oggetti ADSI. Le funzioni principali includono la fornitura di un punto di ingresso in un archivio directory, il caricamento delle proprietà nella cache delle proprietà e il commit delle modifiche nella directory sottostante.
-   [Schema](schema-interfaces.md). Queste interfacce forniscono metodi per la gestione e l'estensione dello schema di directory.
-   [Cache delle proprietà](property-cache-interfaces.md). Queste interfacce definiscono metodi per la modifica delle proprietà nella cache delle proprietà.
-   [Oggetto persistente](persistent-object-interfaces.md). Queste interfacce modificano i dati persistenti nello spazio dei nomi del servizio directory sottostante. Gli oggetti ADSI implementano questi tipi di interfacce per fornire l'accesso ai dati persistenti, inclusi account utente, condivisioni file, gerarchie organizzative ed elenchi di processi in una coda di stampa.
-   [Oggetto dinamico](dynamic-object-interfaces.md). Queste interfacce funzionano con i dati dinamici in un servizio directory. Gli oggetti directory non rappresentati nel servizio directory sottostante implementano tali interfacce. Esempi di dati dinamici includono i comandi emessi in rete.
-   [Sicurezza](security-interfaces.md). Queste interfacce consentono a un client ADSI di stabilire le proprie credenziali a un server e di usare le funzionalità di sicurezza supportate dal servizio directory, ad esempio l'elenco di controllo di accesso o i descrittori di sicurezza.
-   [Non di automazione](non-automation-interfaces.md). Queste interfacce consentono ai client non di automazione (ad esempio, applicazioni C/C++) un accesso con sovraccarico ridotto agli oggetti directory fornendo l'accesso Vtable ai metodi per la gestione e la ricerca di oggetti del servizio directory.
-   [Estensione](extension-interfaces.md). Queste interfacce consentono ai client ADSI di estendere le funzionalità delle classi ADSI esistenti per offrire soluzioni personalizzate ai servizi directory.
-   [Utilità](utility-interfaces.md). Queste interfacce forniscono funzioni helper avanzate per la gestione di oggetti ADSI.
-   [Tipo di dati](data-type-interfaces.md). Queste interfacce forniscono metodi per accedere ai tipi di dati ADSI.

 

 




