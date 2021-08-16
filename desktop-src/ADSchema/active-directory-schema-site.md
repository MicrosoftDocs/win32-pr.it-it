---
title: Terminologia dello schema di Active Directory
description: I termini seguenti vengono comunemente usati per fare riferimento allo schema di Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b48256d1df8f9c344fe0acceb2fb6a70ed3033260baea4db7df44dd71e1c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836438"
---
# <a name="active-directory-schema-terminology"></a>Terminologia dello schema di Active Directory

I termini seguenti vengono comunemente usati per fare riferimento allo schema di Active Directory.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo
</dt> <dd>

Elementi di dati utilizzati per descrivere gli oggetti rappresentati dalle classi definite nello schema. Gli attributi vengono definiti nello schema separatamente dalle classi. Ciò consente di applicare una singola definizione di attributo a molte classi. Ad esempio, [**Description**](a-description.md) è un attributo che può essere applicato a qualsiasi classe nello schema. **L'attributo Description** viene definito una sola volta nello schema, assicurando la coerenza, anziché avere una definizione diversa per **Description** of a user (Descrizione di un utente) e **Description** of a printer (Descrizione di una stampante).

> [!Note]  
> Il termine *proprietà viene* spesso usato in modo intercambiabile con il termine *attributo*.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Istanza dell'attributo
</dt> <dd>

Occorrenza di un attributo definito nello schema. Questo termine viene usato per distinguere tra la definizione di un attributo e un'occorrenza discreta dell'attributo. Ad esempio, l'archiviazione di un oggetto User per "Jeff Smith" con l'attributo [**Common-Name**](a-cn.md) impostato su "Jeff Smith" crea un'istanza di [**Common-Name**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Classe
</dt> <dd>

Descrizione formale di un tipo di oggetto discreto e identificabile archiviato nel servizio directory. Ad esempio, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md)e [**Group**](c-group.md) sono tutte classi. Sono inoltre disponibili tre categorie distinte di classi: [classi strutturali,](classes-structural.md)classi [astratte](classes-abstract.md) [e classi ausiliarie.](classes-auxiliary.md)

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Istanza della classe
</dt> <dd>

Occorrenza di una classe definita nello schema. Questo termine viene usato per distinguere tra la definizione di una classe e un'occorrenza discreta della classe. Ad esempio, l'archiviazione [**di un**](c-user.md) oggetto User per "Jeff Smith" nel servizio directory crea un'istanza di [**User**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Regole del contenuto
</dt> <dd>

Definizione del possibile contenuto delle istanze della classe archiviate nel servizio directory. In NT Directory Services (NTDS), su cui si basa Active Directory, le regole del contenuto sono espresse completamente dagli attributi [**Must-Contain**](a-mustcontain.md) e [**May-Contain**](a-maycontain.md) delle definizioni dello schema per ogni classe.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivazione
</dt> <dd>

Vedere *Ereditarietà.*

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Albero delle informazioni sulla directory
</dt> <dd>

La directory stessa, rappresentata come struttura ad albero in cui i vertici sono le voci di directory (istanze di classe) e le linee di connessione le relazioni padre-figlio tra le voci.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>Dit
</dt> <dd>

Vedere *Albero delle informazioni sulla directory.*

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Controllare i diritti di accesso
</dt> <dd>

Classe che descrive un diritto di accesso non associato a una risorsa, ma a un'azione. Ad esempio, a un utente può essere concesso il diritto di creare valori ID relativi.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Eredità
</dt> <dd>

Possibilità di compilare nuove classi di oggetti da classi di oggetti esistenti. Il nuovo oggetto è definito come *sottoclasse* dell'oggetto padre. L'oggetto padre diventa *una superclasse* del nuovo oggetto. Una sottoclasse eredita gli attributi dell'elemento padre, incluse le regole di struttura e di contenuto.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>Ldap
</dt> <dd>

Vedere *Lightweight Directory Access Protocol*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol
</dt> <dd>

Protocollo di comunicazione Internet standard utilizzato per comunicare con NTDS. Sono supportati LDAP versione 2 e versione 3.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descrittore di sicurezza NT
</dt> <dd>

Vedere *Descrittore di sicurezza.*

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Oggetto
</dt> <dd>

Unità di archiviazione dei dati nel servizio directory. Gli oggetti del servizio directory non devono essere confusi con gli oggetti COM o altri oggetti di sistema orientati a oggetti, che hanno un componente eseguibile e un comportamento in fase di esecuzione. Gli oggetti del servizio directory sono costituiti solo da dati. Un oggetto servizio directory viene definito da un oggetto [**Class-Schema**](c-classschema.md) e da un gruppo di oggetti [**Attribute-Schema**](c-attributeschema.md) a cui fa riferimento [**l'oggetto Class-Schema.**](c-classschema.md)

[**Gli oggetti Class-Schema**](c-classschema.md) [**e Attribute-Schema**](c-attributeschema.md) sono a loro volta oggetti del servizio directory e hanno definizioni nello schema come qualsiasi altro oggetto. Vedere *Classe*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificatore di oggetto
</dt> <dd>

Valori numerici univoci, emessi da varie autorità emittente, per identificare in modo univoco gli elementi dati, le sintassi e varie altre parti delle applicazioni distribuite. Gli identificatori di oggetto (OID) si trovano nelle applicazioni OSI, nelle directory X.500, in SNMP e in altre applicazioni in cui l'univocità è importante. Gli OID sono basati su una struttura ad albero, in cui un'autorità emittente superiore, ad esempio l'ISO, alloca un ramo dell'albero a una sotto-autorità, che a sua volta può allocare rami secondari.

Gli OID in NTDS includono alcuni rilasciati dall'ISO per classi e attributi X.500 e altri rilasciati da Microsoft. La notazione OID è una stringa tratteggiata di numeri, ad esempio "1.2.840.113556.1.5.4", che viene tradotta come indicato nell'elenco seguente. 

| Valore  | Descrizione                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO: l'"autorità radice", rilasciata "1.2" ad ANSI, che a sua volta...                           |
| 2      | Ansi... rilasciato "1.2.840" negli Stati Uniti, che a sua volta...                                            |
| 840    | Usa... rilasciato "1.2.840.113556" a Microsoft...                                               |
| 113556 | Microsoft... dove Microsoft gestisce internamente diversi rami OID in "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | Classi NTDS                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>Oid
</dt> <dd>

Vedere *Identificatore di oggetto.*

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema
</dt> <dd>

Definizione formale del contenuto e della struttura del servizio directory. Lo schema definisce tutti gli attributi e le classi. Per ogni classe vengono definiti gli attributi [**Poss-Superiors,**](a-posssuperiors.md) [**Must-Contain**](a-mustcontain.md)e [**May-Contain.**](a-maycontain.md) [**Poss-Superiors**](a-posssuperiors.md) definisce le possibili strutture ad albero per il servizio directory specificando quali classi possono essere padre per qualsiasi classe specificata. [**Must-Contain**](a-mustcontain.md) e [**May-Contain**](a-maycontain.md) elencano gli attributi per una classe che devono essere presenti per archiviare la classe e gli attributi aggiuntivi eventualmente presenti.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descrittore di sicurezza
</dt> <dd>

Informazioni sulla proprietà di un oggetto e sulle autorizzazioni di altri utenti per tale oggetto. La [**proprietà NT-Security-Descriptor**](a-ntsecuritydescriptor.md) di una voce dello schema contiene una stringa che rappresenta il descrittore di sicurezza dell'oggetto. Per altre informazioni sul formato delle informazioni in questo campo, vedere [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Regole di struttura
</dt> <dd>

Definizione della struttura ad albero o delle strutture ad albero possibili. In NTDS le regole di struttura sono espresse completamente dall'attributo Poss-superiors presente in ogni [**oggetto Class-Schema.**](c-classschema.md) Vedere *Schema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Sottoclasse
</dt> <dd>

Oggetto [**Class-Schema**](c-classschema.md) che eredita da un altro [**oggetto Class-Schema.**](c-classschema.md) Vedere *Ereditarietà.*

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclasse
</dt> <dd>

Oggetto [**Class-Schema**](c-classschema.md) da cui ereditano uno o più altri [**oggetti Class-Schema.**](c-classschema.md) Vedere *Ereditarietà.*

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Albero
</dt> <dd>

Vedere *Albero delle informazioni sulla directory.*

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X.500
</dt> <dd>

Famiglia di standard sviluppati congiuntamente da ISO e ITU, precedentemente noti come CCITT, che specificano i protocolli di denominazione, rappresentazione dei dati e comunicazione per un servizio directory.

</dd> </dl>

 

 