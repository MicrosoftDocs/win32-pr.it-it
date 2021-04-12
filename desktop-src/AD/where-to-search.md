---
title: Scelta della posizione in cui eseguire la ricerca
description: In questo argomento vengono illustrate le diverse ricerche che possono essere eseguite in Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidere dove eseguire la ricerca in Active Directory
- Active Directory AD, ricerca, scelta della posizione in cui eseguire la ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336758"
---
# <a name="deciding-where-to-search"></a>Scelta della posizione in cui eseguire la ricerca

In questo argomento vengono illustrate le diverse ricerche che possono essere eseguite in Active Directory Domain Services.

Tutte le ricerche vengono eseguite in uno dei seguenti contesti di denominazione:

-   Dominio, incluse le partizioni di directory applicative
-   Contenitore dello schema
-   Contenitore di configurazione
-   Catalogo globale

## <a name="searching-a-domain"></a>Ricerca in un dominio

I domini contengono la maggior parte degli oggetti altamente usati, ad esempio utenti, contatti, gruppi, unità organizzative, computer e così via. La maggior parte delle query cercherà un dominio. Per ulteriori informazioni sulla ricerca di un dominio, vedere [ricerca di contenuto del dominio](searching-domain-contents.md).

## <a name="searching-the-schema-container"></a>Ricerca nel contenitore dello schema

Il contenitore dello schema contiene gli oggetti [**classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) che forniscono la definizione formale di ogni classe e attributo che può esistere in Active Directory Domain Services. Per cercare gli oggetti nel contenitore dello schema, associare il contenitore dello schema in qualsiasi controller di dominio. Il contenitore dello schema è disponibile in tutti i controller di dominio. Il nome distinto del contenitore dello schema viene ottenuto dall'attributo **schemaNamingContext** di RootDSE. Per ulteriori informazioni su rootDSE e sull'attributo **schemaNamingContext** , vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).

Per ulteriori informazioni sulla lettura dallo schema o dal contenitore dello schema astratto, vedere [linee guida per l'associazione allo schema](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Ricerca nel contenitore di configurazione

Il contenitore di configurazione contiene informazioni di configurazione, ad esempio siti, servizi e identificatori di visualizzazione, per l'intera foresta. Per cercare gli oggetti nel contenitore di configurazione, eseguire l'associazione al contenitore di configurazione in qualsiasi controller di dominio. Il contenitore di configurazione è disponibile in tutti i controller di dominio. Il nome distinto del contenitore di configurazione è ottenuto dall'attributo **configurationNamingContext** di RootDSE. Per ulteriori informazioni su rootDSE e sull'attributo **configurationNamingContext** , vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Ricerca nel catalogo globale

Il catalogo globale include una replica di ogni oggetto in Active Directory Domain Services, ma con un numero ridotto di attributi. Gli attributi nel catalogo globale sono quelli usati più di frequente nelle operazioni di ricerca, ad esempio il nome e il cognome di un utente, i nomi di accesso e così via. Per ulteriori informazioni sulla ricerca nel catalogo globale, vedere la pagina relativa alla [ricerca nel catalogo globale](searching-global-catalog-contents.md).

 

 