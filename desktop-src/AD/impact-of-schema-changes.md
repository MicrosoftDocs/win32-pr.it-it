---
title: Conseguenze delle modifiche dello schema
description: In questo argomento viene descritto il modo in cui un'estensione dello schema influisca sulla foresta Active Directory.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Conseguenze delle modifiche allo schema AD
- ANNUNCIO dello schema, conseguenze della modifica dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45aa43ed208b6eca5889220e09c78e8ada4a50a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297731"
---
# <a name="impact-of-schema-changes"></a>Conseguenze delle modifiche dello schema

Un'estensione dello schema influisca su una foresta di domini controllata da Active Directory Domain Services in diversi modi:

-   Le modifiche dello schema sono globali. Esiste un solo schema per un'intera foresta. Lo schema viene replicato a livello globale: esiste una copia dello schema in ogni controller di dominio della foresta. Quando si estende lo schema, questo viene esteso per l'intera foresta.
-   Impossibile annullare l'aggiunta degli oggetti dello schema. Quando un nuovo oggetto Class o attribute viene aggiunto allo schema, non può essere rimosso. Un attributo o una classe esistente può essere disabilitata, ma non è stata rimossa. Per ulteriori informazioni, vedere la pagina relativa alla [disabilitazione di classi e attributi esistenti](disabling-existing-classes-and-attributes.md). La disabilitazione di una classe o di un attributo non influisce sulle istanze esistenti della classe o dell'attributo, ma impedisce la creazione di nuove istanze. Non è possibile disabilitare un attributo se è incluso in una classe non disabilitata.
-   OID deve essere univoco. Quando un attributo o una classe viene aggiunta allo schema, non è possibile aggiungere alcun attributo o classe con lo stesso OID. Questo vale anche se una classe o un attributo è stato disabilitato. Per questo motivo è necessario usare OID validi. Non sintetizzare un OID e non riutilizzare un OID esistente. Per ulteriori informazioni su come ottenere un OID valido, vedere [ottenere un identificatore di oggetto radice](obtaining-an-object-identifier.md).
-   Dopo la creazione è possibile apportare alcune modifiche:

    -   Per una classe categoria 1 o categoria 2, è possibile aggiungere o rimuovere valori nell'attributo **possSuperiors** . I valori **possSuperiors** specificano le classi di oggetti che possono contenere la classe.
    -   Per una classe categoria 1 o categoria 2, è possibile aggiungere o rimuovere valori nell'attributo **mayContain** . I valori **mayContain** specificano gli attributi facoltativi, ma possono essere presenti in un'istanza della classe.

-   È possibile modificare il valore di **ldapDisplayName** per una classe o un attributo di categoria 2 dopo che è stato creato. In genere, non è consigliabile modificare il **ldapDisplayName**. Tuttavia, esiste un motivo legittimo per modificare il nome LDAP, ovvero se si è verificato un errore durante la definizione dell'attributo o della classe ed è necessario crearne uno nuovo per sostituire quello precedente. Per eseguire questa operazione, non è necessario rinominare il nome distinto relativo (RDN) dell'attributo o dello schema della classe. Quando viene modificato il nome LDAP, è possibile aggirare un errore anziché ricompilare l'intera infrastruttura di Windows 2000. Per ulteriori informazioni, vedere la pagina relativa alla [disabilitazione di classi e attributi esistenti](disabling-existing-classes-and-attributes.md).

    Non è possibile modificare **ldapDisplayName** per le classi o gli attributi predefiniti (categoria 1). Per ulteriori informazioni sugli oggetti dello schema Category 1 e 2, vedere [restrizioni sull'estensione dello schema](restrictions-on-schema-extension.md).

 

 




