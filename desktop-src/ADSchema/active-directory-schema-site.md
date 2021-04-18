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
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="20b44-103">Terminologia dello schema Active Directory</span><span class="sxs-lookup"><span data-stu-id="20b44-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="20b44-104">I termini seguenti sono comunemente utilizzati per fare riferimento allo schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="20b44-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="20b44-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo</span><span class="sxs-lookup"><span data-stu-id="20b44-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="20b44-106">Elementi di dati utilizzati per descrivere gli oggetti rappresentati dalle classi definite nello schema.</span><span class="sxs-lookup"><span data-stu-id="20b44-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="20b44-107">Gli attributi sono definiti separatamente nello schema dalle classi; in questo modo è possibile applicare una singola definizione di attributo a numerose classi.</span><span class="sxs-lookup"><span data-stu-id="20b44-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="20b44-108">La [**Descrizione**](a-description.md) , ad esempio, è un attributo che può essere applicato a qualsiasi classe nello schema.</span><span class="sxs-lookup"><span data-stu-id="20b44-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="20b44-109">L'attributo **Description** viene definito una volta nello schema, garantendo la coerenza, anziché avere una definizione diversa per la **Descrizione** di un utente e una **Descrizione** di una stampante.</span><span class="sxs-lookup"><span data-stu-id="20b44-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="20b44-110">Il termine *Proprietà* viene spesso usato in modo interscambiabile con l' *attributo* term.</span><span class="sxs-lookup"><span data-stu-id="20b44-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="20b44-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Istanza di attributo</span><span class="sxs-lookup"><span data-stu-id="20b44-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="20b44-112">Occorrenza di un attributo definito nello schema.</span><span class="sxs-lookup"><span data-stu-id="20b44-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="20b44-113">Questo termine viene usato per distinguere tra la definizione di un attributo e un'occorrenza discreta dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="20b44-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="20b44-114">Se ad esempio si archivia un oggetto utente per "Jeff Smith" con l'attributo [**nome comune**](a-cn.md) impostato su "Jeff Smith", viene creata un'istanza di [**nome comune**](a-cn.md).</span><span class="sxs-lookup"><span data-stu-id="20b44-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="20b44-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Classe</span><span class="sxs-lookup"><span data-stu-id="20b44-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="20b44-116">Descrizione formale di un tipo discreto e identificabile di un oggetto archiviato nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="20b44-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="20b44-117">Ad esempio, l' [**utente**](c-user.md), la [**coda di stampa**](c-printqueue.md)e il [**gruppo**](c-group.md) sono tutte classi.</span><span class="sxs-lookup"><span data-stu-id="20b44-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="20b44-118">Sono inoltre disponibili 3 categorie distinte di classi, ovvero [classi strutturali](classes-structural.md), [classi astratte](classes-abstract.md)e [classi ausiliarie](classes-auxiliary.md).</span><span class="sxs-lookup"><span data-stu-id="20b44-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="20b44-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Istanza della classe</span><span class="sxs-lookup"><span data-stu-id="20b44-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="20b44-120">Occorrenza di una classe definita nello schema.</span><span class="sxs-lookup"><span data-stu-id="20b44-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="20b44-121">Questo termine viene usato per distinguere tra la definizione di una classe e un'occorrenza discreta della classe.</span><span class="sxs-lookup"><span data-stu-id="20b44-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="20b44-122">Se ad esempio si archivia un oggetto [**utente**](c-user.md) per "Jeff Smith" nel servizio directory, viene creata un'istanza dell' [**utente**](c-user.md).</span><span class="sxs-lookup"><span data-stu-id="20b44-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="20b44-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Regole contenuto</span><span class="sxs-lookup"><span data-stu-id="20b44-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="20b44-124">Definizione del contenuto possibile delle istanze della classe archiviate nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="20b44-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="20b44-125">In NT Directory Services (NTDS), su cui si basa Active Directory, le regole di contenuto sono completamente espresse dagli attributi [**must-contain**](a-mustcontain.md) e [**may-contain**](a-maycontain.md) delle definizioni dello schema per ogni classe.</span><span class="sxs-lookup"><span data-stu-id="20b44-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivazione</span><span class="sxs-lookup"><span data-stu-id="20b44-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="20b44-127">Vedere *ereditarietà*.</span><span class="sxs-lookup"><span data-stu-id="20b44-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Albero delle informazioni di directory</span><span class="sxs-lookup"><span data-stu-id="20b44-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="20b44-129">La directory stessa, rappresentata come una struttura ad albero in cui i vertici sono le voci di directory (istanze della classe) e le linee di connessione delle relazioni padre-figlio tra le voci.</span><span class="sxs-lookup"><span data-stu-id="20b44-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-130"><span id="DIT"></span><span id="dit"></span>DIT</span><span class="sxs-lookup"><span data-stu-id="20b44-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="20b44-131">Vedere *albero delle informazioni di directory*.</span><span class="sxs-lookup"><span data-stu-id="20b44-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Controllo dei diritti di accesso</span><span class="sxs-lookup"><span data-stu-id="20b44-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="20b44-133">Classe che descrive un diritto di accesso non associato a una risorsa, ma un'azione.</span><span class="sxs-lookup"><span data-stu-id="20b44-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="20b44-134">È ad esempio possibile concedere a un utente il diritto di creare valori ID relativi.</span><span class="sxs-lookup"><span data-stu-id="20b44-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Ereditarietà</span><span class="sxs-lookup"><span data-stu-id="20b44-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="20b44-136">Possibilità di compilare nuove classi di oggetti da classi di oggetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="20b44-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="20b44-137">Il nuovo oggetto viene definito come *sottoclasse* dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="20b44-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="20b44-138">L'oggetto padre diventa una *superclasse* del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="20b44-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="20b44-139">Una sottoclasse eredita gli attributi dell'elemento padre, incluse le regole di struttura e di contenuto.</span><span class="sxs-lookup"><span data-stu-id="20b44-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span><span class="sxs-lookup"><span data-stu-id="20b44-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="20b44-141">Vedere *Lightweight Directory Access Protocol*.</span><span class="sxs-lookup"><span data-stu-id="20b44-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span><span class="sxs-lookup"><span data-stu-id="20b44-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="20b44-143">Protocollo di comunicazione Internet standard usato per comunicare con NTDS.</span><span class="sxs-lookup"><span data-stu-id="20b44-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="20b44-144">Sono supportate le versioni LDAP 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="20b44-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descrittore di sicurezza NT</span><span class="sxs-lookup"><span data-stu-id="20b44-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="20b44-146">Vedere *descrittore di sicurezza*.</span><span class="sxs-lookup"><span data-stu-id="20b44-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Oggetto</span><span class="sxs-lookup"><span data-stu-id="20b44-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="20b44-148">Unità di archiviazione dei dati nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="20b44-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="20b44-149">Gli oggetti del servizio directory non devono essere confusi con oggetti COM o altri oggetti di sistema orientati a oggetti, che hanno un componente eseguibile e un comportamento in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="20b44-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="20b44-150">Gli oggetti del servizio directory sono costituiti solo da dati.</span><span class="sxs-lookup"><span data-stu-id="20b44-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="20b44-151">Un oggetto servizio directory è definito da un oggetto [**dello schema della classe**](c-classschema.md) e da un gruppo di oggetti [**schema attributo**](c-attributeschema.md) a cui fa riferimento l'oggetto di [**schema classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="20b44-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="20b44-152">Gli oggetti schema [**class**](c-classschema.md) e [**attribute-schema**](c-attributeschema.md) sono stessi oggetti del servizio di directory e presentano definizioni nello schema come qualsiasi altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="20b44-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="20b44-153">Vedere la *classe*.</span><span class="sxs-lookup"><span data-stu-id="20b44-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificatore oggetto</span><span class="sxs-lookup"><span data-stu-id="20b44-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="20b44-155">Valori numerici univoci, emessi da varie autorità emittenti, per identificare in modo univoco elementi dati, sintassi e varie altre parti di applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="20b44-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="20b44-156">Gli identificatori di oggetto (OID) si trovano in applicazioni OSI, directory X. 500, SNMP e altre applicazioni in cui l'unicità è importante.</span><span class="sxs-lookup"><span data-stu-id="20b44-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="20b44-157">OID sono basati su una struttura ad albero, in cui un'autorità emittente superiore, ad esempio l'immagine ISO, alloca un ramo della struttura ad albero a un'autorità secondaria, che a sua volta può allocare sottorami.</span><span class="sxs-lookup"><span data-stu-id="20b44-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="20b44-158">OID nel NTDS includono alcuni rilasciati dall'ISO per le classi e gli attributi X. 500 e alcuni rilasciati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20b44-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="20b44-159">La notazione OID è una stringa punteggiata di numeri, ad esempio "1.2.840.113556.1.5.4", che viene convertita come elencato nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="20b44-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="20b44-160">Valore</span><span class="sxs-lookup"><span data-stu-id="20b44-160">Value</span></span>  | <span data-ttu-id="20b44-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20b44-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20b44-162">1</span><span class="sxs-lookup"><span data-stu-id="20b44-162">1</span></span>      | <span data-ttu-id="20b44-163">ISO: "autorità radice", emesso "1,2" in ANSI, che a sua volta...</span><span class="sxs-lookup"><span data-stu-id="20b44-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="20b44-164">2</span><span class="sxs-lookup"><span data-stu-id="20b44-164">2</span></span>      | <span data-ttu-id="20b44-165">ANSI... ha emesso "1.2.840" per gli Stati Uniti, che a loro volta...</span><span class="sxs-lookup"><span data-stu-id="20b44-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="20b44-166">840</span><span class="sxs-lookup"><span data-stu-id="20b44-166">840</span></span>    | <span data-ttu-id="20b44-167">STATI UNITI... "1.2.840.113556" è stato emesso a Microsoft...</span><span class="sxs-lookup"><span data-stu-id="20b44-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="20b44-168">113556</span><span class="sxs-lookup"><span data-stu-id="20b44-168">113556</span></span> | <span data-ttu-id="20b44-169">Microsoft... dove Microsoft gestisce internamente diversi rami OID in "1.2.840.113556".</span><span class="sxs-lookup"><span data-stu-id="20b44-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="20b44-170">1</span><span class="sxs-lookup"><span data-stu-id="20b44-170">1</span></span>      | <span data-ttu-id="20b44-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="20b44-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="20b44-172">5</span><span class="sxs-lookup"><span data-stu-id="20b44-172">5</span></span>      | <span data-ttu-id="20b44-173">Classi NTDS</span><span class="sxs-lookup"><span data-stu-id="20b44-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="20b44-174">4</span><span class="sxs-lookup"><span data-stu-id="20b44-174">4</span></span>      | <span data-ttu-id="20b44-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="20b44-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="20b44-176"><span id="OID"></span><span id="oid"></span>OID</span><span class="sxs-lookup"><span data-stu-id="20b44-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="20b44-177">Vedere *identificatore di oggetto*.</span><span class="sxs-lookup"><span data-stu-id="20b44-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span><span class="sxs-lookup"><span data-stu-id="20b44-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="20b44-179">Definizione formale della struttura e del contenuto del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="20b44-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="20b44-180">Lo schema definisce tutti gli attributi e le classi.</span><span class="sxs-lookup"><span data-stu-id="20b44-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="20b44-181">Per ogni classe, vengono definiti gli attributi [**poss-Superior**](a-posssuperiors.md), [**must-contain**](a-mustcontain.md)e [**possono contenere**](a-maycontain.md) .</span><span class="sxs-lookup"><span data-stu-id="20b44-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="20b44-182">[**Poss-Superior**](a-posssuperiors.md) definisce le strutture ad albero possibili per il servizio directory specificando quali classi possono essere l'elemento padre di una determinata classe.</span><span class="sxs-lookup"><span data-stu-id="20b44-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="20b44-183">[**Must-contain**](a-mustcontain.md) e [**possono contenere**](a-maycontain.md) l'elenco degli attributi per una classe che deve essere presente per archiviare la classe e quali attributi aggiuntivi possono eventualmente essere presenti.</span><span class="sxs-lookup"><span data-stu-id="20b44-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="20b44-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="20b44-185">Informazioni sulla proprietà di un oggetto e sulle autorizzazioni che altri utenti hanno su tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="20b44-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="20b44-186">La proprietà [**NT-Security-descrittore**](a-ntsecuritydescriptor.md) di una voce di schema contiene una stringa che rappresenta il descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="20b44-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="20b44-187">Per ulteriori informazioni sul formato delle informazioni in questo campo, vedere il [formato della stringa del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="20b44-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="20b44-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Regole struttura</span><span class="sxs-lookup"><span data-stu-id="20b44-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="20b44-189">La definizione della struttura ad albero o delle strutture possibili.</span><span class="sxs-lookup"><span data-stu-id="20b44-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="20b44-190">In NTDS le regole della struttura sono completamente espresse dall'attributo poss-superiors presente in ogni oggetto [**dello schema della classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="20b44-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="20b44-191">Vedere *schema*.</span><span class="sxs-lookup"><span data-stu-id="20b44-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Sottoclasse</span><span class="sxs-lookup"><span data-stu-id="20b44-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="20b44-193">Oggetto [**dello schema della classe**](c-classschema.md) che eredita da un altro oggetto [**dello schema della classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="20b44-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="20b44-194">Vedere *ereditarietà*.</span><span class="sxs-lookup"><span data-stu-id="20b44-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclasse</span><span class="sxs-lookup"><span data-stu-id="20b44-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="20b44-196">Oggetto [**dello schema di classe**](c-classschema.md) da cui ereditano uno o più oggetti [**dello schema della classe**](c-classschema.md) .</span><span class="sxs-lookup"><span data-stu-id="20b44-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="20b44-197">Vedere *ereditarietà*.</span><span class="sxs-lookup"><span data-stu-id="20b44-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Albero</span><span class="sxs-lookup"><span data-stu-id="20b44-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="20b44-199">Vedere *albero delle informazioni di directory*.</span><span class="sxs-lookup"><span data-stu-id="20b44-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="20b44-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="20b44-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="20b44-201">Gruppo di standard sviluppato congiuntamente da ISO e ITU, in precedenza noto come CCITT, che specificano i protocolli di denominazione, rappresentazione dei dati e comunicazione per un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="20b44-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 