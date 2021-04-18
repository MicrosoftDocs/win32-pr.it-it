---
title: Sintassi del filtro di ricerca
description: I filtri di ricerca consentono di definire criteri di ricerca e forniscono ricerche più efficienti ed efficaci.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Sintassi del filtro di ricerca ADSI
- query, sintassi del filtro di ricerca
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334000"
---
# <a name="search-filter-syntax"></a><span data-ttu-id="58d78-105">Sintassi del filtro di ricerca</span><span class="sxs-lookup"><span data-stu-id="58d78-105">Search Filter Syntax</span></span>

<span data-ttu-id="58d78-106">I filtri di ricerca consentono di definire criteri di ricerca e forniscono ricerche più efficienti ed efficaci.</span><span class="sxs-lookup"><span data-stu-id="58d78-106">Search filters enable you to define search criteria and provide more efficient and effective searches.</span></span>

<span data-ttu-id="58d78-107">ADSI supporta i filtri di ricerca LDAP come definito in RFC2254.</span><span class="sxs-lookup"><span data-stu-id="58d78-107">ADSI supports the LDAP search filters as defined in RFC2254.</span></span> <span data-ttu-id="58d78-108">Questi filtri di ricerca sono rappresentati da stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="58d78-108">These search filters are represented by Unicode strings.</span></span> <span data-ttu-id="58d78-109">Nella tabella seguente sono elencati alcuni esempi di filtri di ricerca LDAP.</span><span class="sxs-lookup"><span data-stu-id="58d78-109">The following table lists some examples of LDAP search filters.</span></span>



| <span data-ttu-id="58d78-110">Filtro di ricerca</span><span class="sxs-lookup"><span data-stu-id="58d78-110">Search filter</span></span>                                                               | <span data-ttu-id="58d78-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58d78-111">Description</span></span>                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="58d78-112">"(objectClass = \* )"</span><span class="sxs-lookup"><span data-stu-id="58d78-112">"(objectClass=\*)"</span></span>                                                          | <span data-ttu-id="58d78-113">Tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="58d78-113">All objects.</span></span>                                               |
| <span data-ttu-id="58d78-114">"(& (objectCategory = person) (objectClass = user) (! ( CN = Andy))) "</span><span class="sxs-lookup"><span data-stu-id="58d78-114">"(&(objectCategory=person)(objectClass=user)(!(cn=andy)))"</span></span>                  | <span data-ttu-id="58d78-115">Tutti gli oggetti utente, ma "Andy".</span><span class="sxs-lookup"><span data-stu-id="58d78-115">All user objects but "andy".</span></span>                               |
| <span data-ttu-id="58d78-116">"(SN = SM \* )"</span><span class="sxs-lookup"><span data-stu-id="58d78-116">"(sn=sm\*)"</span></span>                                                                 | <span data-ttu-id="58d78-117">Tutti gli oggetti con un cognome che inizia con "SM".</span><span class="sxs-lookup"><span data-stu-id="58d78-117">All objects with a surname that starts with "sm".</span></span>          |
| <span data-ttu-id="58d78-118">"(& (objectCategory = person) (objectClass = Contact) ( \| (sn = Smith) (sn = Johnson)))"</span><span class="sxs-lookup"><span data-stu-id="58d78-118">"(&(objectCategory=person)(objectClass=contact)(\|(sn=Smith)(sn=Johnson)))"</span></span> | <span data-ttu-id="58d78-119">Tutti i contatti con cognome uguale a "Smith" o "Johnson".</span><span class="sxs-lookup"><span data-stu-id="58d78-119">All contacts with a surname equal to "Smith" or "Johnson".</span></span> |



 

<span data-ttu-id="58d78-120">Questi filtri di ricerca usano uno dei formati seguenti.</span><span class="sxs-lookup"><span data-stu-id="58d78-120">These search filters use one of the following formats.</span></span>


```C++
<filter>=(<attribute><operator><value>)
```



<span data-ttu-id="58d78-121">oppure</span><span class="sxs-lookup"><span data-stu-id="58d78-121">or</span></span>


```C++
(<operator><filter1><filter2>)
```



<span data-ttu-id="58d78-122">I filtri di ricerca ADSI vengono usati in due modi.</span><span class="sxs-lookup"><span data-stu-id="58d78-122">The ADSI search filters are used in two ways.</span></span> <span data-ttu-id="58d78-123">Formano una parte del dialetto LDAP per l'invio di query tramite il provider di OLE DB.</span><span class="sxs-lookup"><span data-stu-id="58d78-123">They form a part of the LDAP dialect for submitting queries through the OLE DB provider.</span></span> <span data-ttu-id="58d78-124">Vengono inoltre usati con l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="58d78-124">They are also used with the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

## <a name="operators"></a><span data-ttu-id="58d78-125">Operatori</span><span class="sxs-lookup"><span data-stu-id="58d78-125">Operators</span></span>

<span data-ttu-id="58d78-126">Nella tabella seguente sono elencati gli operatori di filtro di ricerca usati di frequente.</span><span class="sxs-lookup"><span data-stu-id="58d78-126">The following table lists frequently used search filter operators.</span></span>



| <span data-ttu-id="58d78-127">Operatore logico</span><span class="sxs-lookup"><span data-stu-id="58d78-127">Logical operator</span></span> | <span data-ttu-id="58d78-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58d78-128">Description</span></span>                                |
|------------------|--------------------------------------------|
| =                | <span data-ttu-id="58d78-129">Uguale a</span><span class="sxs-lookup"><span data-stu-id="58d78-129">Equal to</span></span>                                   |
| ~=               | <span data-ttu-id="58d78-130">Approssimativamente uguale a</span><span class="sxs-lookup"><span data-stu-id="58d78-130">Approximately equal to</span></span>                     |
| <=            | <span data-ttu-id="58d78-131">Lessicografico minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="58d78-131">Lexicographically less than or equal to</span></span>    |
| >=            | <span data-ttu-id="58d78-132">Lessicografico maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="58d78-132">Lexicographically greater than or equal to</span></span> |
| &                | <span data-ttu-id="58d78-133">AND</span><span class="sxs-lookup"><span data-stu-id="58d78-133">AND</span></span>                                        |
| \|               | <span data-ttu-id="58d78-134">OR</span><span class="sxs-lookup"><span data-stu-id="58d78-134">OR</span></span>                                         |
| <span data-ttu-id="58d78-135">!</span><span class="sxs-lookup"><span data-stu-id="58d78-135">!</span></span>                | <span data-ttu-id="58d78-136">NOT</span><span class="sxs-lookup"><span data-stu-id="58d78-136">NOT</span></span>                                        |



 

<span data-ttu-id="58d78-137">Oltre agli operatori precedenti, LDAP definisce due identificatori di oggetto regola (OID) corrispondenti che possono essere usati per eseguire confronti bit per bit di valori numerici.</span><span class="sxs-lookup"><span data-stu-id="58d78-137">In addition to the operators above, LDAP defines two matching rule object identifiers (OIDs) that can be used to perform bitwise comparisons of numeric values.</span></span> <span data-ttu-id="58d78-138">Le regole di corrispondenza hanno la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="58d78-138">Matching rules have the following syntax.</span></span>


```C++
<attribute name>:<matching rule OID>:=<value>
```



<span data-ttu-id="58d78-139">" &lt; nome attributo &gt; " è l' **ldapDisplayName** dell'attributo " &lt; Rule OID &gt; " è l'OID per la regola di corrispondenza e " &lt; value &gt; " è il valore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="58d78-139">"&lt;attribute name&gt;" is the **lDAPDisplayName** of the attribute, "&lt;rule OID&gt;" is the OID for the matching rule, and "&lt;value&gt;" is the value to use for comparison.</span></span> <span data-ttu-id="58d78-140">Tenere presente che in questa stringa non è possibile utilizzare spazi.</span><span class="sxs-lookup"><span data-stu-id="58d78-140">Be aware that spaces cannot be used in this string.</span></span> <span data-ttu-id="58d78-141">" &lt; value &gt; " deve essere un numero decimale. non può essere un numero esadecimale o un nome di costante, ad esempio la **\_ sicurezza del tipo di gruppo Ads \_ \_ \_ abilitata**.</span><span class="sxs-lookup"><span data-stu-id="58d78-141">"&lt;value&gt;" must be a decimal number; it cannot be a hexadecimal number or a constant name such as **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED**.</span></span> <span data-ttu-id="58d78-142">Per ulteriori informazioni sugli attributi di Active Directory disponibili, vedere [tutti gli attributi](/windows/desktop/ADSchema/attributes-all).</span><span class="sxs-lookup"><span data-stu-id="58d78-142">For more information about the available Active Directory attributes, see [All Attributes](/windows/desktop/ADSchema/attributes-all).</span></span>

<span data-ttu-id="58d78-143">La tabella seguente elenca la regola di corrispondenza OID implementata da LDAP.</span><span class="sxs-lookup"><span data-stu-id="58d78-143">The following table lists the matching rule OIDs implemented by LDAP.</span></span>



| <span data-ttu-id="58d78-144">OID regola di corrispondenza</span><span class="sxs-lookup"><span data-stu-id="58d78-144">Matching rule OID</span></span>       | <span data-ttu-id="58d78-145">Identificatore di stringa (da Ntldap. h)</span><span class="sxs-lookup"><span data-stu-id="58d78-145">String identifier (from Ntldap.h)</span></span>   | <span data-ttu-id="58d78-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58d78-146">Description</span></span>                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d78-147">1.2.840.113556.1.4.803</span><span class="sxs-lookup"><span data-stu-id="58d78-147">1.2.840.113556.1.4.803</span></span>  | <span data-ttu-id="58d78-148">**\_bit della \_ regola di corrispondenza LDAP \_ \_ e**</span><span class="sxs-lookup"><span data-stu-id="58d78-148">**LDAP\_MATCHING\_RULE\_BIT\_AND**</span></span>  | <span data-ttu-id="58d78-149">Viene trovata una corrispondenza solo se tutti i bit dall'attributo corrispondono al valore.</span><span class="sxs-lookup"><span data-stu-id="58d78-149">A match is found only if all bits from the attribute match the value.</span></span> <span data-ttu-id="58d78-150">Questa regola è equivalente a un operatore **and** bit per bit.</span><span class="sxs-lookup"><span data-stu-id="58d78-150">This rule is equivalent to a bitwise **AND** operator.</span></span>                                                                  |
| <span data-ttu-id="58d78-151">1.2.840.113556.1.4.804</span><span class="sxs-lookup"><span data-stu-id="58d78-151">1.2.840.113556.1.4.804</span></span>  | <span data-ttu-id="58d78-152">**\_bit della regola di corrispondenza LDAP \_ \_ \_ o**</span><span class="sxs-lookup"><span data-stu-id="58d78-152">**LDAP\_MATCHING\_RULE\_BIT\_OR**</span></span>   | <span data-ttu-id="58d78-153">Viene trovata una corrispondenza se i bit dall'attributo corrispondono al valore.</span><span class="sxs-lookup"><span data-stu-id="58d78-153">A match is found if any bits from the attribute match the value.</span></span> <span data-ttu-id="58d78-154">Questa regola è equivalente a un operatore **OR bit per** bit.</span><span class="sxs-lookup"><span data-stu-id="58d78-154">This rule is equivalent to a bitwise **OR** operator.</span></span>                                                                        |
| <span data-ttu-id="58d78-155">1.2.840.113556.1.4.1941</span><span class="sxs-lookup"><span data-stu-id="58d78-155">1.2.840.113556.1.4.1941</span></span> | <span data-ttu-id="58d78-156">**\_ \_ regola di corrispondenza LDAP \_ nella \_ catena**</span><span class="sxs-lookup"><span data-stu-id="58d78-156">**LDAP\_MATCHING\_RULE\_IN\_CHAIN**</span></span> | <span data-ttu-id="58d78-157">Questa regola è limitata ai filtri applicati al DN.</span><span class="sxs-lookup"><span data-stu-id="58d78-157">This rule is limited to filters that apply to the DN.</span></span> <span data-ttu-id="58d78-158">Si tratta di uno speciale operatore di corrispondenza "esteso" che percorre la catena di origini negli oggetti fino alla radice fino a quando non viene trovata una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="58d78-158">This is a special "extended" match operator that walks the chain of ancestry in objects all the way to the root until it finds a match.</span></span> |



 

<span data-ttu-id="58d78-159">La stringa di query di esempio seguente cerca gli oggetti gruppo per i quali è impostato il flag di **\_ \_ \_ sicurezza \_ abilitata per il tipo di gruppo ADS** .</span><span class="sxs-lookup"><span data-stu-id="58d78-159">The following example query string searches for group objects that have the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** flag set.</span></span> <span data-ttu-id="58d78-160">Tenere presente che per il valore di confronto viene usato il valore decimale della **\_ sicurezza del tipo di gruppo Ads \_ \_ \_ abilitata** (0x80000000 = 2147483648).</span><span class="sxs-lookup"><span data-stu-id="58d78-160">Be aware that the decimal value of **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) is used for the comparison value.</span></span>


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



<span data-ttu-id="58d78-161">La **\_ regola di corrispondenza LDAP \_ \_ nella \_ catena** è un OID della regola di corrispondenza progettato per fornire un metodo per cercare l'origine di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="58d78-161">The **LDAP\_MATCHING\_RULE\_IN\_CHAIN** is a matching rule OID that is designed to provide a method to look up the ancestry of an object.</span></span> <span data-ttu-id="58d78-162">Molte applicazioni che usano Active Directory e AD LDS in genere funzionano con i dati gerarchici, ordinati in base alle relazioni padre-figlio.</span><span class="sxs-lookup"><span data-stu-id="58d78-162">Many applications using AD and AD LDS usually work with hierarchical data, which is ordered by parent-child relationships.</span></span> <span data-ttu-id="58d78-163">In precedenza, le applicazioni eseguivano un'espansione del gruppo transitiva per determinare l'appartenenza al gruppo, che usava troppa larghezza di banda di rete; le applicazioni devono creare più round trip per determinare se un oggetto è caduto "nella catena" Se un collegamento viene attraversato fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="58d78-163">Previously, applications performed transitive group expansion to figure out group membership, which used too much network bandwidth; applications needed to make multiple roundtrips to figure out if an object fell "in the chain" if a link is traversed through to the end.</span></span>

<span data-ttu-id="58d78-164">Un esempio di query di questo tipo è quello progettato per verificare se un utente "User1" è un membro del gruppo "group1".</span><span class="sxs-lookup"><span data-stu-id="58d78-164">An example of such a query is one designed to check if a user "user1" is a member of group "group1".</span></span> <span data-ttu-id="58d78-165">Impostare la base sul DN dell'utente `(cn=user1, cn=users, dc=x)` e l'ambito su `base` e usare la query seguente.</span><span class="sxs-lookup"><span data-stu-id="58d78-165">You would set the base to the user DN `(cn=user1, cn=users, dc=x)` and the scope to `base`, and use the following query.</span></span>


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



<span data-ttu-id="58d78-166">Analogamente, per trovare tutti i gruppi di cui "User1" è membro, impostare la base sul DN del contenitore gruppi; ad esempio `(OU=groupsOU, dc=x)` e l'ambito di `subtree` e usare il filtro seguente.</span><span class="sxs-lookup"><span data-stu-id="58d78-166">Similarly, to find all the groups that "user1" is a member of, set the base to the groups container DN; for example `(OU=groupsOU, dc=x)` and the scope to `subtree`, and use the following filter.</span></span>


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



<span data-ttu-id="58d78-167">Si noti che quando si usa la **\_ \_ regola di corrispondenza LDAP \_ nella \_ catena**, l'ambito non è limitato, ovvero può essere `base` , `one-level` o `subtree` .</span><span class="sxs-lookup"><span data-stu-id="58d78-167">Note that when using **LDAP\_MATCHING\_RULE\_IN\_CHAIN**, scope is not limited—it can be `base`, `one-level`, or `subtree`.</span></span> <span data-ttu-id="58d78-168">Alcune query su sottoalberi potrebbero richiedere un maggior numero di processori, ad esempio la ricerca di collegamenti con un fan-out elevato; ovvero, elencando tutti i gruppi di cui un utente è membro.</span><span class="sxs-lookup"><span data-stu-id="58d78-168">Some such queries on subtrees may be more processor intensive, such as chasing links with a high fan-out; that is, listing all the groups that a user is a member of.</span></span> <span data-ttu-id="58d78-169">Le ricerche inefficienti registreranno i messaggi appropriati del registro eventi, come per qualsiasi altro tipo di query.</span><span class="sxs-lookup"><span data-stu-id="58d78-169">Inefficient searches will log appropriate event log messages, as with any other type of query.</span></span>

## <a name="wildcards"></a><span data-ttu-id="58d78-170">Caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="58d78-170">Wildcards</span></span>

<span data-ttu-id="58d78-171">È anche possibile aggiungere caratteri jolly e Condizioni a un filtro di ricerca LDAP.</span><span class="sxs-lookup"><span data-stu-id="58d78-171">You can also add wildcards and conditions to an LDAP search filter.</span></span> <span data-ttu-id="58d78-172">Gli esempi seguenti illustrano le sottostringhe che possono essere usate per eseguire ricerche nella directory.</span><span class="sxs-lookup"><span data-stu-id="58d78-172">The following examples show substrings that can be used to search the directory.</span></span>

<span data-ttu-id="58d78-173">Ottenere tutte le voci:</span><span class="sxs-lookup"><span data-stu-id="58d78-173">Get all entries:</span></span>


```C++
(objectClass=*)
```



<span data-ttu-id="58d78-174">Ottenere le voci contenenti "Bob" in un punto qualsiasi nel nome comune:</span><span class="sxs-lookup"><span data-stu-id="58d78-174">Get entries containing "bob" somewhere in the common name:</span></span>


```C++
(cn=*bob*)
```



<span data-ttu-id="58d78-175">Ottenere le voci con un nome comune maggiore o uguale a "Bob":</span><span class="sxs-lookup"><span data-stu-id="58d78-175">Get entries with a common name greater than or equal to "bob":</span></span>


```C++
(cn>='bob')
```



<span data-ttu-id="58d78-176">Ottenere tutti gli utenti con un attributo di posta elettronica:</span><span class="sxs-lookup"><span data-stu-id="58d78-176">Get all users with an email attribute:</span></span>


```C++
(&(objectClass=user)(email=*))
```



<span data-ttu-id="58d78-177">Ottenere tutte le voci utente con un attributo di posta elettronica e un cognome uguale a "Smith":</span><span class="sxs-lookup"><span data-stu-id="58d78-177">Get all user entries with an email attribute and a surname equal to "smith":</span></span>


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



<span data-ttu-id="58d78-178">Ottenere tutte le voci utente con un nome comune che inizia con "Andy", "Steve" o "Margaret":</span><span class="sxs-lookup"><span data-stu-id="58d78-178">Get all user entries with a common name that starts with "andy", "steve", or "margaret":</span></span>


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



<span data-ttu-id="58d78-179">Ottenere tutte le voci senza un attributo di posta elettronica:</span><span class="sxs-lookup"><span data-stu-id="58d78-179">Get all entries without an email attribute:</span></span>


```C++
(!(email=*))
```



<span data-ttu-id="58d78-180">La definizione formale del filtro di ricerca è la seguente (da [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span><span class="sxs-lookup"><span data-stu-id="58d78-180">The formal definition of the search filter is as follows (from [RFC 2254](https://tools.ietf.org/html/rfc2254)):</span></span>


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



<span data-ttu-id="58d78-181">Il token &lt; attr &gt; è una stringa che rappresenta un attributeType.</span><span class="sxs-lookup"><span data-stu-id="58d78-181">The token &lt;attr&gt; is a string that represents an AttributeType.</span></span> <span data-ttu-id="58d78-182">Il valore del token &lt; &gt; è una stringa che rappresenta un AttributeValue il cui formato è definito dal servizio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="58d78-182">The token &lt;value&gt; is a string that represents an AttributeValue whose format is defined by the underlying directory service.</span></span>

<span data-ttu-id="58d78-183">Se un &lt; valore &gt; deve contenere il carattere asterisco ( \* ), parentesi aperta (() o parentesi destra ()), il carattere deve essere preceduto dal carattere di escape della barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="58d78-183">If a &lt;value&gt; must contain the asterisk (\*), left parenthesis ((), or right parenthesis ()) character, the character should be preceded by the backslash escape character (\\).</span></span>

## <a name="special-characters"></a><span data-ttu-id="58d78-184">Caratteri speciali</span><span class="sxs-lookup"><span data-stu-id="58d78-184">Special Characters</span></span>

<span data-ttu-id="58d78-185">Se uno dei caratteri speciali seguenti deve essere visualizzato nel filtro di ricerca come valori letterali, è necessario sostituirli con la sequenza di escape elencata.</span><span class="sxs-lookup"><span data-stu-id="58d78-185">If any of the following special characters must appear in the search filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="58d78-186">Carattere ASCII</span><span class="sxs-lookup"><span data-stu-id="58d78-186">ASCII character</span></span> | <span data-ttu-id="58d78-187">Sostituzione sequenza di escape</span><span class="sxs-lookup"><span data-stu-id="58d78-187">Escape sequence substitute</span></span> |
|-----------------|----------------------------|
| \*              | <span data-ttu-id="58d78-188">\\2a</span><span class="sxs-lookup"><span data-stu-id="58d78-188">\\2a</span></span>                       |
| <span data-ttu-id="58d78-189">(</span><span class="sxs-lookup"><span data-stu-id="58d78-189">(</span></span>               | <span data-ttu-id="58d78-190">\\28</span><span class="sxs-lookup"><span data-stu-id="58d78-190">\\28</span></span>                       |
| <span data-ttu-id="58d78-191">)</span><span class="sxs-lookup"><span data-stu-id="58d78-191">)</span></span>               | <span data-ttu-id="58d78-192">\\29</span><span class="sxs-lookup"><span data-stu-id="58d78-192">\\29</span></span>                       |
| \\              | <span data-ttu-id="58d78-193">\\5C</span><span class="sxs-lookup"><span data-stu-id="58d78-193">\\5c</span></span>                       |
| <span data-ttu-id="58d78-194">NUL</span><span class="sxs-lookup"><span data-stu-id="58d78-194">NUL</span></span>             | <span data-ttu-id="58d78-195">\\00</span><span class="sxs-lookup"><span data-stu-id="58d78-195">\\00</span></span>                       |
| /               | <span data-ttu-id="58d78-196">\\2F</span><span class="sxs-lookup"><span data-stu-id="58d78-196">\\2f</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="58d78-197">Nei casi in cui viene utilizzato un set di caratteri MultiByte, le sequenze di escape elencate in precedenza devono essere utilizzate se la ricerca viene eseguita da ADO con il sottolinguaggio SQL.</span><span class="sxs-lookup"><span data-stu-id="58d78-197">In cases where a MultiByte Character Set is being used, the escape sequences listed above must be used if the search is performed by ADO with the SQL dialect.</span></span>

 

<span data-ttu-id="58d78-198">Inoltre, i dati binari arbitrari possono essere rappresentati usando la sintassi della sequenza di escape codificando ogni byte di dati binari con la barra rovesciata ( \\ ) seguita da due cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="58d78-198">In addition, arbitrary binary data may be represented by using the escape sequence syntax by encoding each byte of binary data with the backslash (\\) followed by two hexadecimal digits.</span></span> <span data-ttu-id="58d78-199">Ad esempio, il valore a quattro byte 0x00000004 è codificato come \\ 00 00 \\ 00 \\ \\ 04 in una stringa di filtro.</span><span class="sxs-lookup"><span data-stu-id="58d78-199">For example, the four-byte value 0x00000004 is encoded as \\00\\00\\00\\04 in a filter string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58d78-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58d78-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d78-201">Dialetto LDAP</span><span class="sxs-lookup"><span data-stu-id="58d78-201">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="58d78-202">Sottolinguaggio SQL</span><span class="sxs-lookup"><span data-stu-id="58d78-202">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="58d78-203">Ricerca con l'interfaccia IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="58d78-203">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="58d78-204">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="58d78-204">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="58d78-205">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="58d78-205">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 
