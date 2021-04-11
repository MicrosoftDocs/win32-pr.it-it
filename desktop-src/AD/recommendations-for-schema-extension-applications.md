---
title: Suggerimenti per le applicazioni di estensione dello schema
description: Questo argomento include consigli per le applicazioni di estensione dello schema.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Suggerimenti per le applicazioni di estensione dello schema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2393211eb910ce4bc490667398da7f38d212ddcf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117539"
---
# <a name="recommendations-for-schema-extension-applications"></a>Suggerimenti per le applicazioni di estensione dello schema

Oltre ai prerequisiti, per le applicazioni di estensione dello schema sono consigliate le procedure consigliate seguenti:

-   Trovare il master schema. Associare allo schema sul controller di dominio che rappresenta il master schema. Evitare di modificare in modo inutilmente il ruolo di master schema tra controller di dominio. Per eseguire l'associazione al contenitore dello schema nel master schema. Per ulteriori informazioni, vedere [prerequisiti per l'installazione di un'estensione dello schema](prerequisites-for-installing-a-schema-extension.md).
-   Prima di eseguire qualsiasi azione, controllare la proprietà **allowedChildClassesEffective** del contenitore dello schema per verificare che sia possibile creare attributi e/o classi. Se **attributeSchema** e **classSchema** non sono valori in tale proprietà, non si dispone di diritti sufficienti per aggiungere attributi o classi allo schema. Per ulteriori informazioni, vedere [il codice di esempio per verificare la presenza di diritti per la creazione di oggetti dello schema](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Verificare che l'aggiornamento dello schema consentito sia impostato in modo appropriato nel registro di sistema del master schema. Per creare o impostare questo valore, ripristinare lo stato originale come parte della routine di pulizia dell'applicazione. Per ulteriori informazioni sul controllo e sull'impostazione di questo valore, vedere [Abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).
-   Prima di aggiungere attributi o classi, assicurarsi che non esistano già. Se esistono, verificare che siano gli stessi attributi o classi da aggiungere e non un attributo o una classe creata da un utente con sintassi e proprietà diverse che siano incompatibili con gli attributi o le classi.

    Per gli attributi, eseguire una query per **CN**, **attributeId**, **governsID**, **ldapDisplayName** e **schemaIDGUID** per assicurarsi che non siano già in uso. Se si aggiunge un set di attributi collegati (un collegamento diretto, un collegamento indietro), assicurarsi che i **LinkId** non siano già in uso. Eseguire una query per **governsID** perché l'identificatore di oggetto (OID) deve essere univoco tra gli attributi e le classi.

    Per le classi, eseguire una query per **CN**, **governsID**, **attributeId**, **ldapDisplayName** e **schemaIDGUID** per assicurarsi che non siano già in uso. Eseguire una query per **attributeId** perché l'OID deve essere univoco tra classi e attributi.

    Per ulteriori informazioni sulla verifica dei conflitti di denominazione, vedere il [codice di esempio per il rilevamento di conflitti di denominazione dello schema](example-code-for-detecting-schema-naming-collisions.md).

    Se esistono attributi o classi che sono in conflitto con i nuovi attributi o classi, l'applicazione non deve applicare le modifiche dello schema.

-   Se esiste un conflitto di questo tipo, l'applicazione non deve applicare le modifiche dello schema. È possibile che l'amministratore dello schema debba risolvere la collisione, quindi eseguire di nuovo l'applicazione. In alternativa, è possibile usare un **ldapDisplayName** diverso; Tuttavia, tutte le applicazioni che utilizzano l'attributo o l'oggetto devono essere a conoscenza di tale modifica. Per evitare collisioni OID, ottenere un OID da un'autorità di registrazione dei nomi ISO.
-   Se l'applicazione dipende da attributi o classi che ha aggiunto, aggiornare la cache dello schema prima di aggiungere i nuovi attributi o classi che dipendono da tali attributi o classi. Tenere presente che l'attributo operativo **schemaUpdateNow** è sincrono. Ovvero la chiamata al metodo [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) si bloccherà fino a quando non viene aggiornata la cache dello schema. Quando la chiamata restituisce, la cache dello schema è stata aggiornata e i nuovi attributi e/o classi sono accessibili.

    Per ulteriori informazioni su come aggiornare la cache degli schemi, vedere [il codice di esempio per l'aggiornamento della cache dello schema](example-code-for-updating-the-schema-cache.md).

 

 