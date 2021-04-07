---
title: Caratteristiche delle classi di oggetti
description: Ogni classe di oggetti in Active Directory Domain Services è definita da un oggetto classSchema nel contenitore dello schema.
ms.assetid: 88a2b2a3-e8e2-4be1-9784-9709cbea08d6
ms.tgt_platform: multiple
keywords:
- Caratteristiche delle classi di oggetti AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00c7e750d53597d1532d48c3c463315f8a48bd6d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724631"
---
# <a name="characteristics-of-object-classes"></a>Caratteristiche delle classi di oggetti

Ogni classe di oggetti in Active Directory Domain Services è definita da un oggetto **classSchema** nel contenitore dello schema. Gli attributi di un oggetto **classSchema** specificano le caratteristiche della classe, ad esempio:

-   Identificatori di classe: le classi hanno diversi identificatori, tra cui **ldapDisplayName**, che vengono usati dai client LDAP per identificare la classe nei filtri di ricerca e **schemaIDGUID**, usati nei descrittori di sicurezza per controllare l'accesso alla classe.
-   Attributi possibili: la definizione di una classe di oggetti include elenchi degli attributi obbligatori e facoltativi che è possibile impostare in un'istanza della classe.
-   Possibili elementi padre: ogni istanza dell'oggetto, ad eccezione della radice della gerarchia di directory, ha esattamente un elemento padre. La definizione di una classe di oggetti include elenchi di possibili elementi padre, ovvero delle classi di oggetti che possono contenere un'istanza della classe.
-   Superclasse e classi ausiliarie: ogni classe di oggetti (eccetto [*Top*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))) deriva da un'altra classe. Una classe eredita gli attributi possibili e i possibili elementi padre dalle classi sopra di esso nella gerarchia di classi. Una classe può anche avere un numero qualsiasi di classi ausiliarie da cui eredita gli elenchi di possibili attributi. Per ulteriori informazioni, vedere [ereditarietà delle classi nello Schema Active Directory](class-inheritance-in-the-active-directory-schema.md).

La tabella seguente elenca i **ldapDisplayName** e la descrizione degli attributi chiave di un oggetto **classSchema** . Per ulteriori informazioni e per un elenco completo degli attributi obbligatori e facoltativi di un oggetto **classSchema** , vedere [**classSchema**](/windows/desktop/ADSchema/c-classschema).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>lDAPDisplayName</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cn</strong></td>
<td>Ogni oggetto in Active Directory Domain Services dispone di un attributo di denominazione dal quale viene formato il nome distinto relativo (RDN). L'attributo Naming per gli oggetti <strong>classSchema</strong> è <strong>CN</strong> (nome comune). Il valore assegnato a <strong>CN</strong> è il valore che la classe di oggetti avrà come nome RDN. Il <strong>CN</strong> della classe di oggetti <strong>OrganizationalUnit</strong> , ad esempio, è un'unità organizzativa, che verrebbe visualizzata in un nome distinto come CN = Organizational-Unit. Il <strong>CN</strong> deve essere univoco nel contenitore dello schema.</td>
</tr>
<tr class="even">
<td><strong>lDAPDisplayName</strong></td>
<td>Nome usato dai client LDAP, ad esempio il provider LDAP ADSI, per fare riferimento alla classe, ad esempio per specificare la classe in un filtro di ricerca. Il <strong>ldapDisplayName</strong> di una classe deve essere univoco nel contenitore dello schema, il che significa che deve essere univoco in tutti gli oggetti <strong>classSchema</strong> e <strong>attributeSchema</strong> . Per ulteriori informazioni sulla composizione di un <strong>CN</strong> e di un <strong>ldapDisplayName</strong> per una nuova classe, vedere <a href="naming-attributes-and-classes.md">Naming Attributes and</a>Classes.</td>
</tr>
<tr class="odd">
<td><strong>schemaIDGUID</strong></td>
<td>GUID archiviato come stringa di ottetto. Questo GUID identifica in modo univoco la classe. Questo GUID può essere usato nelle voci di controllo di accesso per controllare l'accesso agli oggetti di questa classe. Per ulteriori informazioni, vedere <a href="setting-permissions-on-child-object-operations.md">impostazione delle autorizzazioni per le operazioni sugli oggetti figlio</a>. Al momento della creazione dell'oggetto <strong>classSchema</strong> , il server Active Directory genera questo valore se non è specificato. Se si crea una nuova classe, generare il proprio GUID per ogni classe in modo che tutte le installazioni dell'estensione usino lo stesso <strong>schemaIDGUID</strong> per fare riferimento alla classe.<br/></td>
</tr>
<tr class="even">
<td><strong>adminDisplayName</strong></td>
<td>Nome visualizzato della classe da utilizzare negli strumenti di amministrazione. Se <strong>AdminDisplayName</strong> non viene specificato al momento della creazione di una classe, il sistema utilizza il Common-Name valore come nome visualizzato. Questo nome visualizzato viene utilizzato solo se non esiste un mapping nella proprietà <strong>classDisplayName</strong> dell'identificatore di visualizzazione per la classe. Per altre informazioni, vedere <a href="display-specifiers.md">identificatori di visualizzazione</a> e <a href="class-and-attribute-display-names.md">nomi visualizzati della classe e dell'attributo</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>governsID</strong></td>
<td>OID della classe. Questo valore deve essere univoco tra <strong>governsIDs</strong> di tutti gli oggetti <strong>classSchema</strong> e <strong>AttributeIDs</strong> di tutti gli oggetti <strong>attributeSchema</strong> . Per ulteriori informazioni, vedere <a href="object-identifiers.md">identificatori di oggetto</a>.</td>
</tr>
<tr class="even">
<td><strong>rDnAttId</strong></td>
<td>Identifica l'attributo di denominazione, ovvero l'attributo che fornisce l'RDN per questa classe se diverso da quello predefinito (<strong>CN</strong>). L'utilizzo di un attributo di denominazione diverso da <strong>CN</strong> è sconsigliato. Gli attributi di denominazione devono essere creati dal set noto (OU, CN, O, L e DC) che viene riconosciuto da tutti i client LDAP versione 3. Per ulteriori informazioni, vedere <a href="object-names-and-identities.md">nomi degli oggetti e identità</a> e <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">sintassi per gli attributi in Active Directory Domain Services</a>. Un attributo di denominazione deve avere la sintassi della stringa di directory. Per ulteriori informazioni, vedere <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">sintassi per gli attributi in Active Directory Domain Services</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>mustContain</strong>, <strong>systemMustContain</strong></td>
<td>Coppia di proprietà con più valori che specificano gli attributi che devono essere presenti nelle istanze di questa classe. Si tratta di attributi obbligatori che devono essere presenti durante la creazione e non possono essere cancellati dopo la creazione. Dopo la creazione della classe, queste proprietà non possono essere modificate. Il set completo di attributi obbligatori per una classe è l'Unione dei valori <strong>systemMustContain</strong> e <strong>mustContain</strong> su questa classe e tutte le classi ereditate.<br/></td>
</tr>
<tr class="even">
<td><strong>mayContain</strong>, <strong>systemMayContain</strong></td>
<td>Coppia di proprietà con più valori che specificano gli attributi che possono essere presenti nelle istanze di questa classe. Si tratta di attributi facoltativi che non sono obbligatori e, pertanto, possono essere o meno presenti in un'istanza di questa classe. È possibile aggiungere o rimuovere valori <strong>mayContain</strong> da un oggetto <strong>classSchema</strong> di categoria 1 o di categoria 2 esistente. Prima di rimuovere un valore <strong>mayContain</strong> da un oggetto <strong>classSchema</strong> , è necessario cercare le istanze della classe di oggetti e cancellare tutti i valori per l'attributo da rimuovere. Dopo la creazione della classe, la proprietà <strong>systemMayContain</strong> non può essere modificata. il set completo di attributi facoltativi per una classe è l'Unione dei valori <strong>systemMayContain</strong> e <strong>mayContain</strong> su questa classe e tutte le classi ereditate.<br/></td>
</tr>
<tr class="odd">
<td><strong>possSuperiors</strong>, <strong>systemPossSuperiors</strong></td>
<td>Coppia di proprietà con più valori che specificano le classi strutturali che possono essere elementi padre legali delle istanze di questa classe. Il set completo di possibili valori superiori è l'Unione dei valori <strong>systemPossSuperiors</strong> e <strong>possSuperiors</strong> in questa classe ed eventuali classi strutturali o astratte ereditate. i valori <strong>systemPossSuperiors</strong> e <strong>possSuperiors</strong> non vengono ereditati dalle classi ausiliarie. È possibile aggiungere o rimuovere valori <strong>possSuperiors</strong> da un oggetto <strong>classSchema</strong> di categoria 1 o di categoria 2 esistente. Dopo la creazione della classe, la proprietà <strong>systemPossSuperiors</strong> non può essere modificata.<br/></td>
</tr>
<tr class="even">
<td><strong>objectClassCategory</strong></td>
<td>Valore intero che specifica la categoria della classe. i possibili valori sono i seguenti:
<ul>
<li>Strutturale, vale a dire che è possibile crearne un'istanza nella directory.</li>
<li>Abstract, vale a dire che la classe fornisce una definizione di base di una classe che può essere usata per formare classi strutturali.</li>
<li>Ausiliario, ovvero una classe che può essere usata per estendere la definizione di una classe che eredita da essa, ma non può essere usata per formare una classe da sola.</li>
</ul>
Per altre informazioni, vedere <a href="structural-abstract-and-auxiliary-classes.md">classi strutturali, astratte e ausiliarie</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>subClassOf</strong></td>
<td>OID per la superclasse immediata di questa classe, ovvero la classe da cui deriva questa classe. Per le classi strutturali, <strong>subclassOf</strong> può essere una classe strutturale o astratta.<br/> Per le classi astratte, <strong>subclassOf</strong> può essere solo una classe astratta.<br/> Per le classi ausiliarie, <strong>subclassOf</strong> può essere una classe astratta o ausiliaria.<br/> Se si definisce una nuova classe, verificare che la classe <strong>subclassOf</strong> esista o esista quando la nuova classe viene scritta nella directory. Se la classe non esiste, l'oggetto <strong>classSchema</strong> non viene aggiunto alla directory.<br/></td>
</tr>
<tr class="even">
<td><strong>auxiliaryClass</strong>, <strong>systemAuxiliaryClass</strong></td>
<td>Coppia di proprietà multivalore che specifica le classi ausiliarie da cui questa classe eredita. Il set completo di classi ausiliarie è l'Unione dei valori <strong>systemAuxiliaryClass</strong> e <strong>auxiliaryClass</strong> su questa classe e tutte le classi ereditate. Per un oggetto <strong>classSchema</strong> esistente, i valori possono essere aggiunti alla proprietà <strong>auxiliaryClass</strong> ma non rimossi. Dopo la creazione della classe, la proprietà <strong>systemAuxiliaryClass</strong> non può essere modificata.<br/></td>
</tr>
<tr class="odd">
<td><strong>defaultObjectCategory</strong></td>
<td>Nome distinto di questa classe di oggetti o di una delle relative superclassi. Quando viene creata un'istanza di questa classe di oggetti, il sistema imposta la proprietà <strong>objectCategory</strong> della nuova istanza sul valore specificato nella proprietà <strong>defaultObjectCategory</strong> della relativa classe di oggetti. La proprietà <strong>objectCategory</strong> è una proprietà indicizzata utilizzata per aumentare l'efficienza delle ricerche della classe di oggetti. Se <strong>defaultObjectCategory</strong> non viene specificato quando viene creata una classe, il sistema lo imposta sul nome distinto (DN) dell'oggetto <strong>classSchema</strong> per questa classe. Se questo oggetto verrà spesso sottoposto a query in base al valore di una superclasse invece che alla classe dell'oggetto, è possibile impostare <strong>defaultObjectCategory</strong> sul DN della superclasse. Se, ad esempio, si esegue una sottoclasse di una classe predefinita (categoria 1), la procedura consigliata consiste nell'impostare <strong>defaultObjectCategory</strong> sullo stesso valore della superclasse. Ciò consente all'interfaccia utente standard di &quot; trovare &quot; la sottoclasse.<br/> Per altre informazioni, vedere <a href="object-class-and-object-category.md">classe di oggetti e categoria di oggetti</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>defaultHidingValue</strong></td>
<td>Valore booleano che specifica l'impostazione predefinita della proprietà <strong>showInAdvancedViewOnly</strong> delle nuove istanze di questa classe. Molti oggetti directory non sono interessanti per gli utenti finali. Per impedire a questi oggetti di ingombrare l'interfaccia utente, ogni oggetto dispone di un attributo booleano denominato <strong>showInAdvancedViewOnly</strong>. Se <strong>defaultHidingValue</strong> è impostato su <strong>true</strong>, le nuove istanze degli oggetti sono nascoste negli snap-in amministrativi e nella shell di Windows. Una voce di menu per la classe di oggetti non verrà visualizzata nel <strong>nuovo</strong> menu di scelta rapida degli snap-in di amministrazione, anche se le proprietà appropriate della creazione guidata sono impostate nell'oggetto <strong>displaySpecifier</strong> della classe di oggetti.<br/> Se <strong>defaultHidingValue</strong> è impostato su <strong>false</strong>, le nuove istanze dell'oggetto vengono visualizzate negli snap-in amministrativi e nella shell di Windows. Impostare questa proprietà su <strong>false</strong> per visualizzare le istanze della classe negli snap-in amministrativi e la shell e abilitare una creazione guidata e la relativa voce di menu nel menu <strong>nuovo</strong> degli snap-in amministrativi.<br/> Se il valore <strong>defaultHidingValue</strong> non è impostato, il valore predefinito è <strong>true</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>systemFlags</strong></td>
<td>Valore intero che contiene i flag che definiscono proprietà aggiuntive della classe. Il bit 0x10 identifica una classe di categoria 1 (una classe che fa parte dello schema di base incluso nel sistema). Non è possibile impostare questo bit, il che significa che il bit non è impostato nelle classi di categoria 2 (che sono estensioni dello schema).</td>
</tr>
<tr class="even">
<td><strong>systemOnly</strong></td>
<td>Valore booleano che specifica se la classe può essere modificata solo dal server Active Directory. Solo le classi di sistema possono essere create o eliminate solo dall'agente del sistema di directory (DSA). Le classi solo di sistema sono quelle da cui dipende il sistema per le normali operazioni.</td>
</tr>
<tr class="odd">
<td><strong>defaultSecurityDescriptor</strong></td>
<td>Specifica il descrittore di sicurezza predefinito per i nuovi oggetti di questa classe. Per ulteriori informazioni, vedere <a href="default-security-descriptor.md">descrittore di sicurezza predefinito</a> e modalità di impostazione dei descrittori <a href="how-security-descriptors-are-set-on-new-directory-objects.md">di sicurezza per i nuovi oggetti directory</a>.</td>
</tr>
<tr class="even">
<td><strong>isDefunct</strong></td>
<td>Valore booleano che indica se la classe è inattiva. Per ulteriori informazioni, vedere la pagina relativa alla <a href="disabling-existing-classes-and-attributes.md">disabilitazione di classi e attributi esistenti</a>.</td>
</tr>
<tr class="odd">
<td><strong>description</strong></td>
<td>Descrizione testuale della classe utilizzata dalle applicazioni amministrative.</td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifica la classe di oggetti di cui questo oggetto è un'istanza, ovvero la classe di oggetti <strong>classSchema</strong> per tutte le definizioni di classe e la classe di oggetti <strong>attributeSchema</strong> per tutte le definizioni di attributo.</td>
</tr>
</tbody>
</table>



 

 

