---
title: Implementazione dello schema
description: In Active Directory Domain Services, le definizioni di classe e attributo vengono archiviate nella directory rispettivamente come istanze delle classi classSchema e attributeSchema.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025019"
---
# <a name="schema-implementation"></a>Implementazione dello schema

In Active Directory Domain Services, le definizioni di classe e attributo vengono archiviate nella directory rispettivamente come istanze delle classi [**classSchema**](/windows/desktop/ADSchema/c-classschema) [**e attributeSchema.**](/windows/desktop/ADSchema/c-attributeschema) **classSchema** **e attributeSchema** sono classi definite nello schema. Per modificare lo schema di Active Directory, usare le stesse operazioni LDAP usate per modificare altri oggetti. Poiché lo schema è una parte chiave della directory che interessa l'intera foresta, si applicano restrizioni speciali alle estensioni dello schema. Per altre informazioni sulle restrizioni, vedere [Restrizioni sulle estensioni dello schema](restrictions-on-schema-extension.md).

Per riepilogare l'implementazione dello schema:

-   Le istanze della [**classe classSchema**](/windows/desktop/ADSchema/c-classschema) definiscono ogni classe di oggetto supportata da Active Directory Domain Services. Gli attributi di un oggetto **classSchema,** ad esempio gli attributi [**mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain,**](/windows/desktop/ADSchema/a-mustcontain) descrivono una classe di oggetti, nello stesso modo in cui gli attributi di un oggetto utente, ad esempio gli attributi [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) e [**telephoneNumber,**](/windows/desktop/ADSchema/a-telephonenumber) descrivono tale utente. Per altre informazioni, vedere [Caratteristiche delle classi di oggetti](characteristics-of-object-classes.md).
-   Le istanze della [**classe attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) vengono usate per definire ogni attributo supportato da Active Directory Domain Services. Gli attributi di un **oggetto attributeSchema,** ad esempio gli attributi **attributeSyntax** e **isSingleValued,** descrivono un attributo, nello stesso modo in cui gli attributi di un oggetto utente descrivono l'utente. Per altre informazioni, vedere [Caratteristiche degli attributi](characteristics-of-attributes.md).
-   Le istanze delle [**classi attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) e [**classSchema**](/windows/desktop/ADSchema/c-classschema) vengono archiviate in una posizione nota nella directory, il contenitore dello schema. Il contenitore dello schema ha sempre un nome distinto nel formato:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    dove "DC=forestroot" è il nome distinto della radice della foresta, ad esempio &lt; &gt; "DC=Fabrikam,DC=Com".

    Per ottenere il nome distinto del contenitore dello schema, leggere **l'attributo schemaNamingContext** di rootDSE. Per altre informazioni su rootDSE e sui relativi attributi, vedere [Associazione serverless e RootDSE](serverless-binding-and-rootdse.md).

Quando si pensa allo schema, tenere presente quanto seguente:

-   Le modifiche dello schema sono globali. Esiste un singolo schema per un'intera foresta. Lo schema viene replicato a livello globale: una copia dello schema esiste in ogni controller di dominio nella foresta. Quando si estende lo schema, si esegue questa operazione per l'intera foresta.
-   Le aggiunte dello schema non sono reversibili. Quando una nuova classe o attributo viene aggiunto allo schema, non può essere rimosso. Un attributo o una classe esistente può essere disabilitato, ma non rimosso. Per altre informazioni, vedere [Disabilitazione di classi e attributi esistenti.](disabling-existing-classes-and-attributes.md)
-   La disabilitazione di una classe o di un attributo non influisce sulle istanze esistenti della classe o dell'attributo, ma impedisce la creazione di nuove istanze. Non è possibile disabilitare un attributo se è incluso in qualsiasi classe non disabilitata.

 

 