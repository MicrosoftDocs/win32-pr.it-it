---
title: Consigli per le applicazioni di estensione dello schema
description: Questo argomento include raccomandazioni per le applicazioni di estensione dello schema.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Consigli per le applicazioni di estensione dello schema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0a01e68fbe9751b778caa2404d02afb1ddd7704457c9cf0aedcc914387ab5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025269"
---
# <a name="recommendations-for-schema-extension-applications"></a>Consigli per le applicazioni di estensione dello schema

Oltre ai prerequisiti, per le applicazioni di estensione dello schema sono consigliate le procedure consigliate seguenti:

-   Trovare il master dello schema. Eseguire l'associazione allo schema nel controller di dominio che è il master schema. Evitare di modificare inutilmente il ruolo master dello schema tra i controller di dominio. Per eseguire l'associazione al contenitore dello schema nel master schema. Per altre informazioni, vedere [Prerequisiti per l'installazione di un'estensione dello schema](prerequisites-for-installing-a-schema-extension.md).
-   Prima di eseguire qualsiasi azione, controllare la **proprietà allowedChildClassesEffective** del contenitore dello schema per verificare che sia possibile creare attributi e/o classi. Se **attributeSchema** e **classSchema** non sono valori in tale proprietà, non si dispone di diritti sufficienti per aggiungere attributi o classi allo schema. Per altre informazioni, vedere [Codice di esempio per il controllo dei diritti per la creazione di oggetti dello schema](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Assicurarsi che l'opzione Aggiornamento dello schema consentito sia impostata in modo appropriato nel Registro di sistema del master schema. Per creare o impostare questo valore, ripristinarlo allo stato originale come parte della routine di pulizia dell'applicazione. Per altre informazioni sul controllo e sull'impostazione di questo valore, vedere [Abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).
-   Prima di aggiungere attributi o classi, assicurarsi che non esistano già. Se esistono, verificare che siano gli stessi attributi o classi aggiunti e non un attributo o una classe creata da un utente con sintassi e proprietà diverse incompatibili con gli attributi o le classi.

    Per gli attributi, eseguire una query per **cn**, **attributeID**, **governsID**, **lDAPDisplayName** e **schemaIDGUID** per assicurarsi che non siano già usati. Se si aggiunge un set di attributi collegati (un collegamento in avanti, un collegamento indietro), assicurarsi che **i linkID** non siano già usati. Eseguire una query **per governsID** perché l'identificatore di oggetto (OID) deve essere univoco tra attributi e classi.

    Per le classi, eseguire una query per **cn**, **governsID**, **attributeID**, **lDAPDisplayName** e **schemaIDGUID** per assicurarsi che non siano già usate. Eseguire una query **per attributeID** perché l'OID deve essere univoco tra classi e attributi.

    Per altre informazioni sul controllo dei conflitti di denominazione, vedere Codice di esempio per il rilevamento dei conflitti di [denominazione degli schemi](example-code-for-detecting-schema-naming-collisions.md).

    Se esistono attributi o classi in conflitto con i nuovi attributi o classi, l'applicazione non deve applicare le modifiche dello schema.

-   Se esiste una collisione di questo tipo, l'applicazione non deve applicare le modifiche dello schema. L'amministratore dello schema potrebbe dover risolvere il conflitto e quindi eseguire di nuovo l'applicazione. In alternativa, è possibile **usare un lDAPDisplayName** diverso. Tuttavia, tutte le applicazioni che usano l'attributo o l'oggetto devono essere a conoscenza di tale modifica. Per evitare conflitti OID, ottenere un OID da un'autorità di registrazione dei nomi ISO.
-   Se l'applicazione dipende da attributi o classi che ha aggiunto, aggiornare la cache dello schema prima di aggiungere i nuovi attributi o classi dipendenti da tali attributi o classi. Tenere presente che **l'attributo operativo schemaUpdateNow** è sincrono. Ciò significa che la chiamata al metodo [**IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) verrà bloccata fino all'aggiornamento della cache dello schema. Quando la chiamata viene restituita, la cache dello schema è stata aggiornata e i nuovi attributi e/o classi sono accessibili.

    Per altre informazioni su come aggiornare la cache dello schema, vedere [Codice di esempio per l'aggiornamento della cache dello schema](example-code-for-updating-the-schema-cache.md).

 

 