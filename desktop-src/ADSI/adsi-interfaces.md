---
title: Interfacce ADSI
description: In questo argomento vengono descritte le categorie utilizzate per le interfacce ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI Interfaces ADSI
- ADSI ADSI, informazioni di riferimento, interfacce
- interfacce ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2930292defa99301fb74f37c933a9af24b73f1fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395310"
---
# <a name="adsi-interfaces"></a>Interfacce ADSI

Active Directory Service Interfaces (ADSI) supporta un set completo di interfacce che possono essere classificate in base alle categorie seguenti:

-   Componenti di [base](core-interfaces.md). Queste interfacce forniscono le funzioni di base di gestione oggetti degli oggetti ADSI. Le funzioni principali includono la fornitura di un punto di ingresso in un archivio directory, il caricamento delle proprietà nella cache delle proprietà e il commit delle modifiche nella directory sottostante.
-   [Schema](schema-interfaces.md). Queste interfacce forniscono metodi per la gestione e l'estensione dello schema di directory.
-   [Cache delle proprietà](property-cache-interfaces.md). Queste interfacce definiscono i metodi per la modifica delle proprietà nella cache delle proprietà.
-   [Oggetto permanente](persistent-object-interfaces.md). Queste interfacce modificano i dati persistenti nello spazio dei nomi del servizio directory sottostante. Gli oggetti ADSI implementano questi tipi di interfacce per fornire l'accesso ai dati persistenti, inclusi gli account utente, le condivisioni file, le gerarchie organizzative e gli elenchi di processi in una coda di stampa.
-   [Oggetto dinamico](dynamic-object-interfaces.md). Queste interfacce funzionano con i dati dinamici in un servizio directory. Gli oggetti directory non rappresentati nel servizio directory sottostante implementano tali interfacce. Esempi di dati dinamici includono i comandi rilasciati in una rete.
-   [Sicurezza](security-interfaces.md). Queste interfacce consentono a un client ADSI di stabilire le proprie credenziali a un server e di utilizzare le funzionalità di sicurezza supportate dal servizio directory, ad esempio l'elenco di controllo di accesso o i descrittori di sicurezza.
-   [Non automazione](non-automation-interfaces.md). Queste interfacce consentono ai client non di automazione (ad esempio, applicazioni C/C++) di accedere in modo ridotto agli oggetti directory fornendo l'accesso vtable ai metodi per la gestione e la ricerca di oggetti del servizio directory.
-   [Estensione](extension-interfaces.md). Queste interfacce consentono ai client ADSI di estendere le funzionalità delle classi ADSI esistenti per offrire soluzioni personalizzate ai servizi directory.
-   [Utilità](utility-interfaces.md). Queste interfacce forniscono funzioni helper avanzate per la gestione degli oggetti ADSI.
-   [Tipo di dati](data-type-interfaces.md). Queste interfacce forniscono metodi per accedere ai tipi di dati ADSI.

 

 




