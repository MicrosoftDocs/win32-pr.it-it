---
title: Definizione di un nuovo attributo
description: In questo argomento viene illustrato come definire un nuovo attributo quando si estende lo schema di Active Directory.
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- Definizione di un nuovo attributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1a0a003d92fe09f27043098cb1abc4387b81e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117570"
---
# <a name="defining-a-new-attribute"></a>Definizione di un nuovo attributo

In questo argomento viene illustrato come definire un nuovo attributo quando si estende lo schema di Active Directory.

Quando si definisce un nuovo attributo, tenere presente quanto segue:

-   Usare gli attributi esistenti quando possibile.
-   Usare sempre la proprietà **CN** (nome comune) come attributo Naming (nome distinto relativo). Si tratta dell'impostazione predefinita per la maggior parte delle classi, incluse quelle derivate direttamente dall'inizio. La proprietà **CN** è una proprietà indicizzata e renderà più efficiente la ricerca di oggetti in base al nome.
-   Gli attributi multivalore di grandi dimensioni sono costosi da archiviare e recuperare e devono essere evitati. Active Directory Domain Services implementare un'estensione LDAP per abilitare la lettura incrementale di proprietà di grandi dimensioni con più valori, ma non tutti i client LDAP riconoscono questa estensione.
-   Tenere presente che gli attributi sono Flat, ovvero non esiste alcuna sottostruttura implicita per un attributo. Tutti gli attributi in una determinata classe devono essere correlati direttamente alle istanze di tale classe.

## <a name="creating-a-new-attribute"></a>Creazione di un nuovo attributo

Per creare un nuovo attributo:

-   Scegliere un nome per l'attributo. Il nome sarà contenuto negli attributi **CN** e **ldapDisplayName** . Per ulteriori informazioni sulla composizione di un nome per un nuovo attributo, vedere [Naming Attributes and classes](naming-attributes-and-classes.md).
-   Ottenere un identificatore di oggetto (OID) per l'attributo. Per ulteriori informazioni, vedere [ottenere un identificatore di oggetto radice](obtaining-an-object-identifier.md).
-   Scegliere una sintassi per l'attributo. La sintassi è determinata dalla combinazione degli attributi **oMSyntax** e **oMObjectClass** . Per ulteriori informazioni, vedere [scelta di una sintassi](choosing-a-syntax.md).
-   Decidere se l'attributo è a valore singolo o multivalore. L'attributo **isSingleValued** determina se l'attributo è a valore singolo o multivalore.
-   Decidere se l'attributo deve essere indicizzato per impostazione predefinita. Per ulteriori informazioni, vedere [attributi indicizzati](indexed-attributes.md).
-   Decidere se l'attributo deve trovarsi nel catalogo globale per impostazione predefinita. Per ulteriori informazioni, vedere [attributi inclusi nel catalogo globale](attributes-included-in-the-global-catalog.md).
-   Se l'attributo è un Integer o una stringa, decidere se è necessario un limite di intervallo. Gli attributi **RangeLower** e **rangeUpper** vengono usati per specificare il limite di intervallo.
-   Se l'attributo è con valori DN, decidere se l'attributo deve essere collegato a un altro attributo. In tal caso, l'attributo [**LinkId**](/windows/desktop/ADSchema/a-linkid) deve essere impostato in modo appropriato su ogni attributo; un attributo deve essere un collegamento in secondo piano, l'altro un collegamento indietro. Per ulteriori informazioni sugli attributi collegati, vedere [attributi collegati](linked-attributes.md).
-   Creare un nuovo oggetto **attributeSchema** nel contenitore dello schema e impostare gli attributi appropriati per l'oggetto. È possibile impostare un numero elevato di attributi per un oggetto **attributeSchema** , ma gli attributi elencati nella tabella seguente sono fondamentali per la definizione di un nuovo attributo. I valori di questi attributi sono determinati dai passaggi precedenti. Per ulteriori informazioni su questi attributi, vedere [caratteristiche degli attributi](characteristics-of-attributes.md).

    | Attributo                                    | Commento                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **cn**<br/>                            | Obbligatorio.<br/>                                 |
    | **lDAPDisplayName**<br/>               | Obbligatorio.<br/>                                 |
    | **adminDisplayName**<br/>              | Obbligatorio.<br/>                                 |
    | **attributeSyntax**<br/>               | Obbligatorio.<br/>                                 |
    | **oMSyntax**<br/>                      | Obbligatorio.<br/>                                 |
    | **oMObjectClass**<br/>                 | Obbligatorio.<br/>                                 |
    | **schemaIDGUID**<br/>                  | Obbligatorio.<br/>                                 |
    | **Elemento AttributeID**<br/>                   | Obbligatorio.<br/>                                 |
    | **isSingleValued**<br/>                | Obbligatorio.<br/>                                 |
    | **searchFlags**<br/>                   | Obbligatorio.<br/>                                 |
    | **isMemberOfPartialAttributeSet**<br/> | Obbligatorio.<br/>                                 |
    | **rangeLower**<br/>                    | facoltativo.<br/>                                 |
    | **rangeUpper**<br/>                    | facoltativo.<br/>                                 |
    | **linkID**<br/>                        | facoltativo. Obbligatorio per gli attributi collegati.<br/> |
    | **description**<br/>                   | facoltativo.<br/>                                 |

    

     

-   Eseguire il commit del nuovo oggetto **attributeSchema** nel contenitore dello schema.
-   Se necessario, aggiornare la cache dello schema. Per ulteriori informazioni, vedere [aggiornamento della cache dello schema](updating-the-schema-cache.md).

 

