---
title: Implementazione dello schema
description: In Active Directory Domain Services, le definizioni di classi e attributi vengono archiviate nella directory come istanze delle classi classSchema e attributeSchema, rispettivamente.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ff18046841b5603be235266e33a7252049f93c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046488"
---
# <a name="schema-implementation"></a>Implementazione dello schema

In Active Directory Domain Services, le definizioni di classi e attributi vengono archiviate nella directory come istanze delle classi [**classSchema**](/windows/desktop/ADSchema/c-classschema) e [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) , rispettivamente. **classSchema** e **attributeSchema** sono classi definite nello schema. Per modificare lo schema di Active Directory, utilizzare le stesse operazioni LDAP utilizzate per modificare altri oggetti. Poiché lo schema è una parte fondamentale della directory che influiscono sull'intera foresta, le restrizioni speciali si applicano alle estensioni dello schema. Per ulteriori informazioni sulle restrizioni, vedere [restrizioni sulle estensioni dello schema](restrictions-on-schema-extension.md).

Per riepilogare l'implementazione dello schema:

-   Le istanze della classe [**classSchema**](/windows/desktop/ADSchema/c-classschema) definiscono ogni classe di oggetti supportata da Active Directory Domain Services. Gli attributi di un oggetto **classSchema** , ad esempio gli attributi [**mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) , descrivono una classe di oggetti, nello stesso modo in cui gli attributi di un oggetto utente, ad esempio gli attributi [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) e [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) , descrivono tale utente. Per ulteriori informazioni, vedere [caratteristiche delle classi di oggetti](characteristics-of-object-classes.md).
-   Le istanze della classe [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) vengono usate per definire ogni attributo supportato da Active Directory Domain Services. Gli attributi di un oggetto **attributeSchema** , ad esempio gli attributi **attributeSyntax** e **isSingleValued** , descrivono un attributo, nello stesso modo in cui gli attributi di un oggetto utente descrivono tale utente. Per ulteriori informazioni, vedere [caratteristiche degli attributi](characteristics-of-attributes.md).
-   Le istanze delle classi [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) e [**classSchema**](/windows/desktop/ADSchema/c-classschema) vengono archiviate in un luogo noto nella directory, ovvero il contenitore dello schema. Il contenitore dello schema ha sempre un nome distinto nel formato:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    dove " &lt; DC = forestroot &gt; " è il nome distinto della radice della foresta, ad esempio, "DC = Fabrikam, DC = com".

    Per ottenere il nome distinto del contenitore dello schema, leggere l'attributo **schemaNamingContext** di RootDSE. Per ulteriori informazioni su rootDSE e sui relativi attributi, vedere [binding senza server e RootDSE](serverless-binding-and-rootdse.md).

Quando si pensa allo schema, tenere presente quanto segue:

-   Le modifiche dello schema sono globali. Esiste un solo schema per un'intera foresta. Lo schema viene replicato a livello globale: esiste una copia dello schema in ogni controller di dominio della foresta. Quando si estende lo schema, questa operazione viene eseguita per l'intera foresta.
-   Le aggiunte dello schema non sono reversibili. Quando una nuova classe o attributo viene aggiunto allo schema, non è possibile rimuoverlo. Un attributo o una classe esistente può essere disabilitata, ma non è stata rimossa. Per ulteriori informazioni, vedere la pagina relativa alla [disabilitazione di classi e attributi esistenti](disabling-existing-classes-and-attributes.md).
-   La disabilitazione di una classe o di un attributo non influisce sulle istanze esistenti della classe o dell'attributo, ma impedisce la creazione di nuove istanze. Non è possibile disabilitare un attributo se è incluso in una classe non disabilitata.

 

 