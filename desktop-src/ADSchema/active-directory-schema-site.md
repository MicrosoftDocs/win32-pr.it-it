---
title: Terminologia dello schema Active Directory
description: I termini seguenti sono comunemente utilizzati per fare riferimento allo schema di Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300690"
---
# <a name="active-directory-schema-terminology"></a>Terminologia dello schema Active Directory

I termini seguenti sono comunemente utilizzati per fare riferimento allo schema di Active Directory.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo
</dt> <dd>

Elementi di dati utilizzati per descrivere gli oggetti rappresentati dalle classi definite nello schema. Gli attributi sono definiti separatamente nello schema dalle classi; in questo modo è possibile applicare una singola definizione di attributo a numerose classi. La [**Descrizione**](a-description.md) , ad esempio, è un attributo che può essere applicato a qualsiasi classe nello schema. L'attributo **Description** viene definito una volta nello schema, garantendo la coerenza, anziché avere una definizione diversa per la **Descrizione** di un utente e una **Descrizione** di una stampante.

> [!Note]  
> Il termine *Proprietà* viene spesso usato in modo interscambiabile con l' *attributo* term.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Istanza di attributo
</dt> <dd>

Occorrenza di un attributo definito nello schema. Questo termine viene usato per distinguere tra la definizione di un attributo e un'occorrenza discreta dell'attributo. Se ad esempio si archivia un oggetto utente per "Jeff Smith" con l'attributo [**nome comune**](a-cn.md) impostato su "Jeff Smith", viene creata un'istanza di [**nome comune**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Classe
</dt> <dd>

Descrizione formale di un tipo discreto e identificabile di un oggetto archiviato nel servizio directory. Ad esempio, l' [**utente**](c-user.md), la [**coda di stampa**](c-printqueue.md)e il [**gruppo**](c-group.md) sono tutte classi. Sono inoltre disponibili 3 categorie distinte di classi, ovvero [classi strutturali](classes-structural.md), [classi astratte](classes-abstract.md)e [classi ausiliarie](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Istanza della classe
</dt> <dd>

Occorrenza di una classe definita nello schema. Questo termine viene usato per distinguere tra la definizione di una classe e un'occorrenza discreta della classe. Se ad esempio si archivia un oggetto [**utente**](c-user.md) per "Jeff Smith" nel servizio directory, viene creata un'istanza dell' [**utente**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Regole contenuto
</dt> <dd>

Definizione del contenuto possibile delle istanze della classe archiviate nel servizio directory. In NT Directory Services (NTDS), su cui si basa Active Directory, le regole di contenuto sono completamente espresse dagli attributi [**must-contain**](a-mustcontain.md) e [**may-contain**](a-maycontain.md) delle definizioni dello schema per ogni classe.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivazione
</dt> <dd>

Vedere *ereditarietà*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Albero delle informazioni di directory
</dt> <dd>

La directory stessa, rappresentata come una struttura ad albero in cui i vertici sono le voci di directory (istanze della classe) e le linee di connessione delle relazioni padre-figlio tra le voci.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>DIT
</dt> <dd>

Vedere *albero delle informazioni di directory*.

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Controllo dei diritti di accesso
</dt> <dd>

Classe che descrive un diritto di accesso non associato a una risorsa, ma un'azione. È ad esempio possibile concedere a un utente il diritto di creare valori ID relativi.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Ereditarietà
</dt> <dd>

Possibilità di compilare nuove classi di oggetti da classi di oggetti esistenti. Il nuovo oggetto viene definito come *sottoclasse* dell'oggetto padre. L'oggetto padre diventa una *superclasse* del nuovo oggetto. Una sottoclasse eredita gli attributi dell'elemento padre, incluse le regole di struttura e di contenuto.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>LDAP
</dt> <dd>

Vedere *Lightweight Directory Access Protocol*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol
</dt> <dd>

Protocollo di comunicazione Internet standard usato per comunicare con NTDS. Sono supportate le versioni LDAP 2 e 3.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descrittore di sicurezza NT
</dt> <dd>

Vedere *descrittore di sicurezza*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Oggetto
</dt> <dd>

Unità di archiviazione dei dati nel servizio directory. Gli oggetti del servizio directory non devono essere confusi con oggetti COM o altri oggetti di sistema orientati a oggetti, che hanno un componente eseguibile e un comportamento in fase di esecuzione. Gli oggetti del servizio directory sono costituiti solo da dati. Un oggetto servizio directory è definito da un oggetto [**dello schema della classe**](c-classschema.md) e da un gruppo di oggetti [**schema attributo**](c-attributeschema.md) a cui fa riferimento l'oggetto di [**schema classe**](c-classschema.md) .

Gli oggetti schema [**class**](c-classschema.md) e [**attribute-schema**](c-attributeschema.md) sono stessi oggetti del servizio di directory e presentano definizioni nello schema come qualsiasi altro oggetto. Vedere la *classe*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificatore oggetto
</dt> <dd>

Valori numerici univoci, emessi da varie autorità emittenti, per identificare in modo univoco elementi dati, sintassi e varie altre parti di applicazioni distribuite. Gli identificatori di oggetto (OID) si trovano in applicazioni OSI, directory X. 500, SNMP e altre applicazioni in cui l'unicità è importante. OID sono basati su una struttura ad albero, in cui un'autorità emittente superiore, ad esempio l'immagine ISO, alloca un ramo della struttura ad albero a un'autorità secondaria, che a sua volta può allocare sottorami.

OID nel NTDS includono alcuni rilasciati dall'ISO per le classi e gli attributi X. 500 e alcuni rilasciati da Microsoft. La notazione OID è una stringa punteggiata di numeri, ad esempio "1.2.840.113556.1.5.4", che viene convertita come elencato nell'elenco seguente. 

| Valore  | Descrizione                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO: "autorità radice", emesso "1,2" in ANSI, che a sua volta...                           |
| 2      | ANSI... ha emesso "1.2.840" per gli Stati Uniti, che a loro volta...                                            |
| 840    | STATI UNITI... "1.2.840.113556" è stato emesso a Microsoft...                                               |
| 113556 | Microsoft... dove Microsoft gestisce internamente diversi rami OID in "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | Classi NTDS                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

Vedere *identificatore di oggetto*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema
</dt> <dd>

Definizione formale della struttura e del contenuto del servizio directory. Lo schema definisce tutti gli attributi e le classi. Per ogni classe, vengono definiti gli attributi [**poss-Superior**](a-posssuperiors.md), [**must-contain**](a-mustcontain.md)e [**possono contenere**](a-maycontain.md) . [**Poss-Superior**](a-posssuperiors.md) definisce le strutture ad albero possibili per il servizio directory specificando quali classi possono essere l'elemento padre di una determinata classe. [**Must-contain**](a-mustcontain.md) e [**possono contenere**](a-maycontain.md) l'elenco degli attributi per una classe che deve essere presente per archiviare la classe e quali attributi aggiuntivi possono eventualmente essere presenti.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descrittore di sicurezza
</dt> <dd>

Informazioni sulla proprietà di un oggetto e sulle autorizzazioni che altri utenti hanno su tale oggetto. La proprietà [**NT-Security-descrittore**](a-ntsecuritydescriptor.md) di una voce di schema contiene una stringa che rappresenta il descrittore di sicurezza dell'oggetto. Per ulteriori informazioni sul formato delle informazioni in questo campo, vedere il [formato della stringa del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Regole struttura
</dt> <dd>

La definizione della struttura ad albero o delle strutture possibili. In NTDS le regole della struttura sono completamente espresse dall'attributo poss-superiors presente in ogni oggetto [**dello schema della classe**](c-classschema.md) . Vedere *schema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Sottoclasse
</dt> <dd>

Oggetto [**dello schema della classe**](c-classschema.md) che eredita da un altro oggetto [**dello schema della classe**](c-classschema.md) . Vedere *ereditarietà*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclasse
</dt> <dd>

Oggetto [**dello schema di classe**](c-classschema.md) da cui ereditano uno o più oggetti [**dello schema della classe**](c-classschema.md) . Vedere *ereditarietà*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Albero
</dt> <dd>

Vedere *albero delle informazioni di directory*.

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X. 500
</dt> <dd>

Gruppo di standard sviluppato congiuntamente da ISO e ITU, in precedenza noto come CCITT, che specificano i protocolli di denominazione, rappresentazione dei dati e comunicazione per un servizio directory.

</dd> </dl>

 

 