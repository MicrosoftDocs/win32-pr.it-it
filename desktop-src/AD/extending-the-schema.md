---
title: Estensione dello schema
description: Lo schema del servizio directory Active Directory definisce gli attributi e le classi utilizzati nel Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo di, schema, estensione dello schema
- ANNUNCIO dello schema, estensione dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299575"
---
# <a name="extending-the-schema"></a>Estensione dello schema

Lo schema del servizio directory Active Directory definisce gli attributi e le classi utilizzati nel Active Directory Domain Services. Lo schema di base incluso nel sistema contiene un set completo di definizioni di classe, ad esempio **User**, **computer** e **OrganizationalUnit**, e le definizioni degli attributi, ad esempio **userPrincipalName**, **telephoneNumber** e **objectSID**. Il set di classi e attributi esistente sarà sufficiente per la maggior parte delle applicazioni. Tuttavia, lo schema è estensibile, il che significa che è possibile definire nuove classi e attributi. In questa sezione viene illustrato come estendere lo schema di Active Directory.

## <a name="when-to-extend-the-schema"></a>Quando estendere lo schema

Se gli attributi e le classi esistenti non rientrano nel tipo di dati che si desidera archiviare, è necessario estendere lo schema. È importante notare che le aggiunte dello schema sono permanenti; è possibile disabilitare classi e attributi, ma non è possibile rimuoverli dallo schema. Tenere presente questo aspetto quando si esegue il test del codice.

Prendere in considerazione anche le dimensioni dei dati che si desidera archiviare. Microsoft consiglia che nessun valore di attributo superi 500 kilobyte, inclusa la somma degli attributi multivalore. Inoltre, le dimensioni degli oggetti non devono superare 1 megabyte. Prendere in considerazione anche il numero di istanze dei dati; Se si aggiunge un nuovo attributo alla classe [**utente**](/windows/desktop/ADSchema/c-user) in un sistema con 100.000 utenti, è possibile che venga utilizzato un notevole spazio.

Gli argomenti di questa sezione includono:

-   Come eseguire l'associazione al contenitore dello schema e leggere le proprietà delle classi e degli attributi esistenti.
-   Come e quando estendere lo schema definendo nuove classi e attributi.
-   Come installare le estensioni dello schema usando LDIFDE, CSVDE o a livello di codice con ADSI.

Per ulteriori informazioni e una panoramica dello schema di Active Directory, incluse informazioni sull'implementazione dello schema, le definizioni delle classi e le definizioni degli attributi, vedere [Active Directory schema](active-directory-schema.md).

Per ulteriori informazioni, incluse le pagine di riferimento per le classi di schema predefinite, gli attributi e le sintassi degli attributi, vedere il riferimento allo schema Active Directory nel [riferimento Active Directory Domain Services](active-directory-domain-services-reference.md).

 

 