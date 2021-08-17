---
title: Estensione dello schema
description: Lo schema del servizio directory Active Directory definisce gli attributi e le classi usati in Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, schema, estensione dello schema
- schema AD, estensione dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c50853e7b782f46b84212965c249ac90b685958c799c1b44cd366d5526e158d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189559"
---
# <a name="extending-the-schema"></a>Estensione dello schema

Lo schema del servizio directory Active Directory definisce gli attributi e le classi usati in Active Directory Domain Services. Lo schema di base incluso nel sistema contiene un set completo di definizioni di classe, ad esempio **user**, **computer** e **organizationalUnit** e definizioni di attributo, ad esempio **userPrincipalName,** **telephoneNumber** e **objectSid**. Il set esistente di classi e attributi sarà sufficiente per la maggior parte delle applicazioni. Tuttavia, lo schema è estendibile, il che significa che è possibile definire nuove classi e attributi. Questa sezione illustra come estendere lo schema di Active Directory.

## <a name="when-to-extend-the-schema"></a>Quando estendere lo schema

Se le classi e gli attributi esistenti non sono adatti al tipo di dati da archiviare, è necessario estendere lo schema. È importante notare che le aggiunte dello schema sono permanenti. È possibile disabilitare classi e attributi, ma non è mai possibile rimuoverli dallo schema. Tenere presente questo problema durante il test del codice.

Considerare anche le dimensioni dei dati da archiviare. Microsoft consiglia che nessun valore di attributo superi 500 kilobyte, inclusa la somma degli attributi multivalore. Inoltre, gli oggetti non devono superare 1 megabyte. Si consideri anche il numero di istanze dei dati. Se si aggiunge un nuovo attributo alla [**classe User**](/windows/desktop/ADSchema/c-user) in un sistema con 100.000 utenti, questo può utilizzare una notevole quantità di spazio.

Gli argomenti di questa sezione includono:

-   Come eseguire l'associazione al contenitore dello schema e leggere le proprietà di classi e attributi esistenti.
-   Come e quando estendere lo schema definendo nuovi attributi e classi.
-   Come installare le estensioni dello schema usando LDIFDE, CSVDE o a livello di codice con ADSI.

Per altre informazioni e una panoramica dello schema di Active Directory, incluse informazioni sull'implementazione dello schema, sulle definizioni di classe e sugli attributi, vedere [Schema di Active Directory.](active-directory-schema.md)

Per altre informazioni, incluse le pagine di riferimento per le classi di schema predefinite, gli attributi e le sintassi degli attributi, vedere le informazioni di riferimento sullo schema di Active Directory in [Active Directory Domain Services.](active-directory-domain-services-reference.md)

 

 