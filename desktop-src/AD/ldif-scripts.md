---
title: Script LDIF
description: LDAP Data Interchange Format (LDIF) è uno standard IETF (Internet Engineering Task Force) che definisce come importare ed esportare i dati della directory tra i server di directory che usano i provider di servizi LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Script LDIF Active Directory
- Active Directory degli script LDIF, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103956213"
---
# <a name="ldif-scripts"></a><span data-ttu-id="bf750-105">Script LDIF</span><span class="sxs-lookup"><span data-stu-id="bf750-105">LDIF Scripts</span></span>

<span data-ttu-id="bf750-106">LDAP Data Interchange Format (LDIF) è uno standard IETF (Internet Engineering Task Force) che definisce come importare ed esportare i dati della directory tra i server di directory che usano i provider di servizi LDAP.</span><span class="sxs-lookup"><span data-stu-id="bf750-106">The LDAP Data Interchange Format (LDIF) is an Internet Engineering Task Force (IETF) standard that defines how to import and export directory data between directory servers that use LDAP service providers.</span></span> <span data-ttu-id="bf750-107">Windows 2000 e Windows Server 2003 includono un'utilità da riga di comando, LDIFDE, che può essere usata per importare oggetti directory in Active Directory Domain Services usando file LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-107">Windows 2000 and Windows Server 2003 include a command-line utility, LDIFDE, which can be used to import directory objects into Active Directory Domain Services using LDIF files.</span></span> <span data-ttu-id="bf750-108">LDIFDE consente di impostare un filtro su una determinata stringa per cercare ed elencare gli oggetti directory in Active Directory Domain Services come file LDIF, che possono essere facilmente letti dagli amministratori dello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-108">LDIFDE enables you to set a filter to a specific string in order to search for and list directory objects in Active Directory Domain Services as LDIF files which can be easily read by schema administrators.</span></span>

<span data-ttu-id="bf750-109">Quando si importa un file Unicode, LDIFDE importa il file come Unicode se contiene l'identificatore Unicode all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="bf750-109">When importing a Unicode file, LDIFDE imports the file as Unicode if it contains the Unicode identifier at the beginning of the file.</span></span> <span data-ttu-id="bf750-110">Se si desidera importare un file come Unicode se non contiene l'identificatore Unicode all'inizio del file, è possibile utilizzare l'opzione-u per forzare l'importazione come Unicode.</span><span class="sxs-lookup"><span data-stu-id="bf750-110">If you wish to import a file as Unicode when it does not contain the Unicode identifier at the beginning of the file, you can use the -u switch in order to force it to be imported as Unicode.</span></span>

<span data-ttu-id="bf750-111">La modalità predefinita per l'esportazione di file è ANSI.</span><span class="sxs-lookup"><span data-stu-id="bf750-111">The default mode for exporting files is ANSI.</span></span> <span data-ttu-id="bf750-112">Se sono presenti voci Unicode, verranno convertite in formato base 64.</span><span class="sxs-lookup"><span data-stu-id="bf750-112">If there are Unicode entries, they will be converted into base 64 format.</span></span> <span data-ttu-id="bf750-113">Per esportare un file in formato Unicode, usare l'opzione-u.</span><span class="sxs-lookup"><span data-stu-id="bf750-113">To export a file into Unicode format, use the -u switch.</span></span>

<span data-ttu-id="bf750-114">Un file LDIF deve applicare modifiche allo schema quando sono presenti dipendenze tra gli attributi aggiunti.</span><span class="sxs-lookup"><span data-stu-id="bf750-114">An LDIF file must apply schema changes when there are dependencies between the attributes that are added.</span></span> <span data-ttu-id="bf750-115">Ad esempio, è necessario aggiungere gli attributi di collegamento diretto prima dell'attributo back link corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bf750-115">For example, forward link attributes should be added before the corresponding back link attribute.</span></span> <span data-ttu-id="bf750-116">Prima di aggiungere classi che dipendono da attributi o classi aggiunte in precedenza nello script LDIF, è necessario aggiornare anche la cache dello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-116">You must also update the schema cache before adding classes that depend on attributes or classes added earlier in the LDIF script.</span></span> <span data-ttu-id="bf750-117">Per ulteriori informazioni, vedere l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="bf750-117">For more information, see the following code example.</span></span>

<span data-ttu-id="bf750-118">Tenere presente che per i valori binari è necessario codificare i valori come Base64.</span><span class="sxs-lookup"><span data-stu-id="bf750-118">Be aware that for binary values, you must encode the values as base64.</span></span> <span data-ttu-id="bf750-119">La codifica Base64 è definita in IETF RFC 2045, sezione 6,8.</span><span class="sxs-lookup"><span data-stu-id="bf750-119">Base64 encoding is defined in IETF RFC 2045, Section 6.8.</span></span>

<span data-ttu-id="bf750-120">Per ulteriori informazioni sul formato dei file LDIF, vedere [la specifica tecnica LDIF (LDAP Data Interchange Format](https://www.ietf.org/rfc/rfc2849.txt) ) (RFC 2849) nel sito Web Internet Engineering Task Force.</span><span class="sxs-lookup"><span data-stu-id="bf750-120">For more information about the format of LDIF files, see [The LDAP Data Interchange Format (LDIF) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) on the Internet Engineering Task Force website.</span></span>

## <a name="ntds-specific-ldif-changetypes"></a><span data-ttu-id="bf750-121">ChangeTypes LDIF specifici per NTDS</span><span class="sxs-lookup"><span data-stu-id="bf750-121">NTDS-specific LDIF changetypes</span></span>

<span data-ttu-id="bf750-122">È preferibile usare ntdsSchema \* ChangeTypes anziché chiamare LDIFDE-k.</span><span class="sxs-lookup"><span data-stu-id="bf750-122">It is better to use ntdsSchema\* changetypes rather than calling ldifde -k.</span></span> <span data-ttu-id="bf750-123">L'opzione-k di LDIFDE ignora un set più ampio di errori LDAP.</span><span class="sxs-lookup"><span data-stu-id="bf750-123">The -k option of ldifde ignores a larger set of LDAP errors.</span></span> <span data-ttu-id="bf750-124">L'elenco completo degli errori ignorati è il seguente:</span><span class="sxs-lookup"><span data-stu-id="bf750-124">The complete list of ignored errors is as follows:</span></span>

-   <span data-ttu-id="bf750-125">L'oggetto è già membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="bf750-125">The object is already a member of the group.</span></span>
-   <span data-ttu-id="bf750-126">Violazione della classe dell'oggetto, ovvero la classe di oggetti specificata non esiste, se l'oggetto importato non ha altri attributi.</span><span class="sxs-lookup"><span data-stu-id="bf750-126">An object class violation (meaning the specified object class does not exist), if the object being imported has no other attributes.</span></span>
-   <span data-ttu-id="bf750-127">l'oggetto esiste già **( \_ LDAP \_ esiste già**)</span><span class="sxs-lookup"><span data-stu-id="bf750-127">object already exists (**LDAP\_ALREADY\_EXISTS**)</span></span>
-   <span data-ttu-id="bf750-128">violazione del vincolo **( \_ \_ violazione del vincolo LDAP**)</span><span class="sxs-lookup"><span data-stu-id="bf750-128">constraint violation (**LDAP\_CONSTRAINT\_VIOLATION**)</span></span>
-   <span data-ttu-id="bf750-129">attributo o valore già esistente (**\_ \_ valore o attributo \_ LDAP \_ esistente**)</span><span class="sxs-lookup"><span data-stu-id="bf750-129">attribute or value already exists (**LDAP\_ATTRIBUTE\_OR\_VALUE\_EXISTS**)</span></span>
-   <span data-ttu-id="bf750-130">nessun oggetto di questo tipo (**LDAP \_ \_ \_**)</span><span class="sxs-lookup"><span data-stu-id="bf750-130">no such object (**LDAP\_NO\_SUCH\_OBJECT**)</span></span>

<span data-ttu-id="bf750-131">I seguenti ChangeTypes sono progettati in modo specifico per le operazioni di aggiornamento dello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-131">The following changetypes are designed specifically for schema upgrade operations.</span></span>



| <span data-ttu-id="bf750-132">ChangeType</span><span class="sxs-lookup"><span data-stu-id="bf750-132">Changetype</span></span>                      | <span data-ttu-id="bf750-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf750-133">Description</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf750-134">**ntdsSchemaAdd**</span><span class="sxs-lookup"><span data-stu-id="bf750-134">**ntdsSchemaAdd**</span></span><br/>    | <span data-ttu-id="bf750-135">**ntdsSchemaAdd** corrisponde a **Aggiungi** in un file LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-135">**ntdsSchemaAdd** corresponds to **add** in an LDIF file.</span></span> <span data-ttu-id="bf750-136">L'unica differenza è che **ntdsSchemaAdd** potrebbe impedire a LDIFDE di ignorare un'operazione di **aggiunta** se l'oggetto esiste già nello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-136">The only difference is that **ntdsSchemaAdd** would cause ldifde to skip an **add** operation if the object already exists in the schema.</span></span> <span data-ttu-id="bf750-137">**LDAP \_ già \_ esistente** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bf750-137">(**LDAP\_ALREADY\_EXISTS** is ignored.)</span></span><br/>                                   |
| <span data-ttu-id="bf750-138">**ntdsSchemaModify**</span><span class="sxs-lookup"><span data-stu-id="bf750-138">**ntdsSchemaModify**</span></span><br/> | <span data-ttu-id="bf750-139">**ntdsSchemaModify** corrisponde alla **modifica** in un file LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-139">**ntdsSchemaModify** corresponds to **modify** in an LDIF file.</span></span> <span data-ttu-id="bf750-140">L'unica differenza è che **ntdsSchemaModify** potrebbe impedire a LDIFDE di ignorare un'operazione di **modifica** se l'oggetto non viene trovato nello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-140">The only difference is that **ntdsSchemaModify** would cause ldifde to skip an **modify** operation if the object is not found in the schema.</span></span> <span data-ttu-id="bf750-141">**LDAP \_ \_ questo \_ oggetto non** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bf750-141">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="bf750-142">**ntdsSchemaDelete**</span><span class="sxs-lookup"><span data-stu-id="bf750-142">**ntdsSchemaDelete**</span></span><br/> | <span data-ttu-id="bf750-143">**ntdsSchemaDelete** corrisponde a **Delete** in un file LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-143">**ntdsSchemaDelete** corresponds to **delete** in an LDIF file.</span></span> <span data-ttu-id="bf750-144">L'unica differenza è che **ntdsSchemaDelete** potrebbe impedire a LDIFDE di ignorare un'operazione di **eliminazione** se l'oggetto non viene trovato nello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-144">The only difference is that **ntdsSchemaDelete** would cause ldifde to skip an **delete** operation if the object is not found in the schema.</span></span> <span data-ttu-id="bf750-145">**LDAP \_ \_ questo \_ oggetto non** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bf750-145">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="bf750-146">**ntdsSchemaModRdn**</span><span class="sxs-lookup"><span data-stu-id="bf750-146">**ntdsSchemaModRdn**</span></span><br/> | <span data-ttu-id="bf750-147">**ntdsSchemaModRdn** corrisponde a **modrdn** in un file LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-147">**ntdsSchemaModRdn** corresponds to **modrdn** in an LDIF file.</span></span> <span data-ttu-id="bf750-148">L'unica differenza è che **ntdsSchemaModRdn** potrebbe impedire a LDIFDE di ignorare un'operazione di modifica, relativa al nome distinto, se l'oggetto non viene trovato nello schema.</span><span class="sxs-lookup"><span data-stu-id="bf750-148">The only difference is that **ntdsSchemaModRdn** would cause ldifde to skip a modify-relative-distinguished-name operation if the object is not found in the schema.</span></span> <span data-ttu-id="bf750-149">**LDAP \_ \_ questo \_ oggetto non** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bf750-149">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/> |



 

## <a name="example"></a><span data-ttu-id="bf750-150">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf750-150">Example</span></span>

<span data-ttu-id="bf750-151">L'esempio di codice seguente include:</span><span class="sxs-lookup"><span data-stu-id="bf750-151">The following code example includes:</span></span>

-   <span data-ttu-id="bf750-152">Myschemaext. ldf è uno script LDIF che contiene nuove classi e attributi.</span><span class="sxs-lookup"><span data-stu-id="bf750-152">Myschemaext.ldf is an LDIF script that contains new attributes and classes.</span></span> <span data-ttu-id="bf750-153">Tenere presente che questo file è una versione modificata del file generato da Lgetattcls.vbs.</span><span class="sxs-lookup"><span data-stu-id="bf750-153">Be aware that this file is a modified version of the file generated from Lgetattcls.vbs.</span></span> <span data-ttu-id="bf750-154">Tenere inoltre presente che l'attributo **My-Test-attribute-DN-FL** è stato spostato in avanti rispetto a **My-Test-attribute-DN-BL** perché il collegamento indietro (**My-Test-attribute-DN-BL**) dipende dal collegamento diretto (**My-Test-attribute-DN-FL**).</span><span class="sxs-lookup"><span data-stu-id="bf750-154">Also be aware that the **My-Test-Attribute-DN-FL** attribute was moved ahead of **My-Test-Attribute-DN-BL** because the back link (**My-Test-Attribute-DN-BL**) is dependent on the forward link (**My-Test-Attribute-DN-FL**).</span></span> <span data-ttu-id="bf750-155">Inoltre, l'attributo operativo **schemaUpdateNow** viene impostato in due posizioni per attivare gli aggiornamenti della cache degli schemi, in modo che gli attributi e le classi dipendenti siano disponibili per aggiungere le due classi nello script.</span><span class="sxs-lookup"><span data-stu-id="bf750-155">Furthermore, the **schemaUpdateNow** operational attribute is set in two places to trigger updates of the schema cache so that dependent attributes and classes will be available for adding the two classes in the script.</span></span>
    > [!Note]  
    > <span data-ttu-id="bf750-156">Vedere l'argomento [ottenere un ID di collegamento](obtaining-a-link-id.md) per informazioni sull'origine dell'ID nelle istruzioni LinkId:.</span><span class="sxs-lookup"><span data-stu-id="bf750-156">See the topic [Obtaining a Link ID](obtaining-a-link-id.md) for information about the source of the ID in the linkID: statements.</span></span>

     

-   <span data-ttu-id="bf750-157">Lgetattcls.vbs è un file VBScript che genera lo script LDIF usato come punto di partenza per Myschemaext. ldf.</span><span class="sxs-lookup"><span data-stu-id="bf750-157">Lgetattcls.vbs is a VBScript file that generates the LDIF script used as the starting point for the Myschemaext.ldf.</span></span> <span data-ttu-id="bf750-158">Tenere presente che il percorso dello schema corrente viene sostituito da CN = schema, CN = Configuration, DC = MyOrg, DC = com.</span><span class="sxs-lookup"><span data-stu-id="bf750-158">Be aware that the current schema path is replaced by CN=Schema,CN=Configuration,DC=myorg,DC=com.</span></span> <span data-ttu-id="bf750-159">È possibile sostituire DC = MyOrg, DC = com per riflettere il nome distinto (DN) da pubblicare nello script LDIF, assicurandosi che LSETATTCLS.VBS rifletta la modifica nel **sFromDN** in modo che il DN corretto venga sostituito quando viene applicato lo script LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-159">You can replace DC=myorg,DC=com to reflect the distinguished name (DN) to publish in the LDIF script  ensure that LSETATTCLS.VBS reflects the change in its **sFromDN** so that the correct DN is replaced when the LDIF script is applied.</span></span> <span data-ttu-id="bf750-160">Tenere inoltre presente che lo script utilizza un prefisso per individuare le classi e gli attributi che è inoltre necessario definire e utilizzare un prefisso per tutte le classi e gli attributi.</span><span class="sxs-lookup"><span data-stu-id="bf750-160">Also be aware that the script uses a prefix to find the classes and attributes you should also define and use a prefix for all your classes and attributes.</span></span> <span data-ttu-id="bf750-161">Per altre informazioni, vedere [Naming Attributes and classes](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="bf750-161">For more information, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span> <span data-ttu-id="bf750-162">Inoltre, lo script restituisce solo gli attributi necessari per gli oggetti **attributeSchema** e **CLASSSCHEMA** al file LDIF.</span><span class="sxs-lookup"><span data-stu-id="bf750-162">In addition, the script outputs only the necessary attributes for the **attributeSchema** and **classSchema** objects to the LDIF file.</span></span>
-   <span data-ttu-id="bf750-163">Lsetattcls.vbs è un file VBScript che usa lo script Myschemaext. ldf per aggiungere i nuovi attributi e le classi nello script.</span><span class="sxs-lookup"><span data-stu-id="bf750-163">Lsetattcls.vbs is a VBScript file that uses the Myschemaext.ldf script to add the new attributes and classes in the script.</span></span> <span data-ttu-id="bf750-164">Verificare che il master schema sia in grado di scrivere prima di eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="bf750-164">Ensure that the schema master is able to be written to before running the script.</span></span>

## <a name="myschemaextldf"></a><span data-ttu-id="bf750-165">MYSCHEMAEXT. LDF</span><span class="sxs-lookup"><span data-stu-id="bf750-165">MYSCHEMAEXT.LDF</span></span>

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a><span data-ttu-id="bf750-166">LGETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="bf750-166">LGETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a><span data-ttu-id="bf750-167">LSETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="bf750-167">LSETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





