---
title: Impatto delle modifiche dello schema
description: Questo argomento descrive come un'estensione dello schema influisce sulla foresta Active Directory.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Impatto delle modifiche dello schema ad Active Directory
- schema AD , impatto della modifica dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa9cc0ee4cdcd0da3581d6bf009837799387949e43dc68989612442352df591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187720"
---
# <a name="impact-of-schema-changes"></a>Impatto delle modifiche dello schema

Un'estensione dello schema influisce su una foresta di dominio Active Directory Domain Services in diversi modi:

-   Le modifiche dello schema sono globali. Esiste un singolo schema per un'intera foresta. Lo schema viene replicato a livello globale: una copia dello schema esiste in ogni controller di dominio nella foresta. Quando si estende lo schema, questo viene esteso per l'intera foresta.
-   Le aggiunte di oggetti dello schema non possono essere annullate. Quando un nuovo oggetto classe o attributo viene aggiunto allo schema, non può essere rimosso. Un attributo o una classe esistente può essere disabilitato, ma non rimosso. Per altre informazioni, vedere [Disabilitazione di classi e attributi esistenti.](disabling-existing-classes-and-attributes.md) La disabilitazione di una classe o di un attributo non influisce sulle istanze esistenti della classe o dell'attributo, ma impedisce la creazione di nuove istanze. Non è possibile disabilitare un attributo se è incluso in qualsiasi classe non disabilitata.
-   Gli OID devono essere univoci. Quando un attributo o una classe viene aggiunto allo schema, non è possibile aggiungere alcun attributo o classe con lo stesso OID. Questo vale anche se una classe o un attributo è stato disabilitato. Per questo motivo è necessario usare OID validi. Non sintetizzare un OID e non riutilizzare un OID esistente. Per altre informazioni su come ottenere un OID valido, vedere [Ottenere un identificatore di oggetto radice](obtaining-an-object-identifier.md).
-   Dopo la creazione, è possibile apportare alcune modifiche:

    -   Per una classe di categoria 1 o 2, è possibile aggiungere o rimuovere valori **nell'attributo possSuperiors.** I **valori possSuperiors** specificano le classi di oggetti che possono contenere la classe .
    -   Per una classe di categoria 1 o di categoria 2, è possibile aggiungere o rimuovere valori **nell'attributo mayContain.** I **valori mayContain** specificano gli attributi facoltativi, ma possono essere presenti in un'istanza della classe .

-   **LDAPDisplayName per** una classe o un attributo di categoria 2 può essere modificato dopo la creazione. In genere, non è consigliabile modificare **lDAPDisplayName**. Esiste tuttavia un motivo legittimo per modificare il nome LDAP, che è stato commesso un errore nella definizione dell'attributo o della classe e deve crearne uno nuovo per sostituire quello precedente. A tale scopo, non è necessario rinominare il nome distinto relativo (RDN) dell'attributo o dello schema di classe. Quando il nome LDAP viene modificato, è possibile risolvere un errore anziché ricompilare l'intera infrastruttura Windows 2000. Per altre informazioni, vedere [Disabilitazione di classi e attributi esistenti.](disabling-existing-classes-and-attributes.md)

    **LDAPDisplayName per** le classi o gli attributi predefiniti (categoria 1) non può essere modificato. Per altre informazioni sugli oggetti dello schema di categoria 1 e 2, vedere [Restrizioni sull'estensione dello schema](restrictions-on-schema-extension.md).

 

 




