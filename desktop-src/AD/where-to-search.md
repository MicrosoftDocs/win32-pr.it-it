---
title: Scelta della posizione in cui eseguire la ricerca
description: Questo argomento illustra le diverse ricerche che possono essere eseguite in Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Scelta della posizione in cui eseguire la ricerca in ACTIVE Directory
- Active Directory AD , Ricerca, Scelta della posizione in cui eseguire la ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6984a79bb761c1926b6735a91209c9f387ac45619ffc752daef253a74f5e587a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024319"
---
# <a name="deciding-where-to-search"></a>Scelta della posizione in cui eseguire la ricerca

Questo argomento illustra le diverse ricerche che possono essere eseguite in Active Directory Domain Services.

Tutte le ricerche vengono eseguite in uno dei contesti di denominazione seguenti:

-   Dominio, incluse le partizioni di directory applicative
-   Contenitore dello schema
-   Contenitore di configurazione
-   Catalogo globale

## <a name="searching-a-domain"></a>Ricerca di un dominio

I domini contengono la maggior parte degli oggetti usati, ad esempio utenti, contatti, gruppi, unità organizzative, computer e così via. La maggior parte delle query esegue la ricerca in un dominio. Per altre informazioni sulla ricerca in un dominio, vedere [Ricerca del contenuto del dominio](searching-domain-contents.md).

## <a name="searching-the-schema-container"></a>Ricerca nel contenitore dello schema

Il contenitore dello schema contiene [**gli oggetti classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) che forniscono la definizione formale di ogni classe e attributo che può esistere in Active Directory Domain Services. Per cercare oggetti nel contenitore dello schema, eseguire il binding al contenitore dello schema in qualsiasi controller di dominio. Il contenitore dello schema è disponibile in tutti i controller di dominio. Il nome distinto del contenitore dello schema viene ottenuto dall'attributo **schemaNamingContext** da rootDSE. Per altre informazioni su rootDSE e **sull'attributo schemaNamingContext,** vedere [Associazione serverless e RootDSE](serverless-binding-and-rootdse.md).

Per altre informazioni sulla lettura dallo schema o dal contenitore dello schema astratto, vedere Linee guida per [l'associazione allo schema](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Ricerca nel contenitore di configurazione

Il contenitore di configurazione contiene informazioni di configurazione, ad esempio siti, servizi e identificatori di visualizzazione, per l'intera foresta. Per cercare oggetti nel contenitore di configurazione, eseguire il binding al contenitore di configurazione in qualsiasi controller di dominio. Il contenitore di configurazione è disponibile in tutti i controller di dominio. Il nome distinto del contenitore di configurazione viene ottenuto **dall'attributo configurationNamingContext** da rootDSE. Per altre informazioni su rootDSE e **sull'attributo configurationNamingContext,** vedere [Associazione serverless e RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Ricerca nel catalogo globale

Il catalogo globale contiene una replica di ogni oggetto Active Directory Domain Services, ma con solo un numero ridotto di attributi. Gli attributi nel catalogo globale sono quelli usati più di frequente nelle operazioni di ricerca, ad esempio il nome e il cognome di un utente, i nomi di accesso e così via. Per altre informazioni sulla ricerca nel catalogo globale, vedere [Ricerca nel catalogo globale](searching-global-catalog-contents.md).

 

 