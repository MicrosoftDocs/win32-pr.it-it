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
# <a name="search-filter-syntax"></a>Sintassi del filtro di ricerca

I filtri di ricerca consentono di definire criteri di ricerca e forniscono ricerche più efficienti ed efficaci.

ADSI supporta i filtri di ricerca LDAP come definito in RFC2254. Questi filtri di ricerca sono rappresentati da stringhe Unicode. Nella tabella seguente sono elencati alcuni esempi di filtri di ricerca LDAP.



| Filtro di ricerca                                                               | Descrizione                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass = \* )"                                                          | Tutti gli oggetti.                                               |
| "(& (objectCategory = person) (objectClass = user) (! ( CN = Andy))) "                  | Tutti gli oggetti utente, ma "Andy".                               |
| "(SN = SM \* )"                                                                 | Tutti gli oggetti con un cognome che inizia con "SM".          |
| "(& (objectCategory = person) (objectClass = Contact) ( \| (sn = Smith) (sn = Johnson)))" | Tutti i contatti con cognome uguale a "Smith" o "Johnson". |



 

Questi filtri di ricerca usano uno dei formati seguenti.


```C++
<filter>=(<attribute><operator><value>)
```



oppure


```C++
(<operator><filter1><filter2>)
```



I filtri di ricerca ADSI vengono usati in due modi. Formano una parte del dialetto LDAP per l'invio di query tramite il provider di OLE DB. Vengono inoltre usati con l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

## <a name="operators"></a>Operatori

Nella tabella seguente sono elencati gli operatori di filtro di ricerca usati di frequente.



| Operatore logico | Descrizione                                |
|------------------|--------------------------------------------|
| =                | Uguale a                                   |
| ~=               | Approssimativamente uguale a                     |
| <=            | Lessicografico minore o uguale a    |
| >=            | Lessicografico maggiore o uguale a |
| &                | AND                                        |
| \|               | OR                                         |
| !                | NOT                                        |



 

Oltre agli operatori precedenti, LDAP definisce due identificatori di oggetto regola (OID) corrispondenti che possono essere usati per eseguire confronti bit per bit di valori numerici. Le regole di corrispondenza hanno la sintassi seguente.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" &lt; nome attributo &gt; " è l' **ldapDisplayName** dell'attributo " &lt; Rule OID &gt; " è l'OID per la regola di corrispondenza e " &lt; value &gt; " è il valore da usare per il confronto. Tenere presente che in questa stringa non è possibile utilizzare spazi. " &lt; value &gt; " deve essere un numero decimale. non può essere un numero esadecimale o un nome di costante, ad esempio la **\_ sicurezza del tipo di gruppo Ads \_ \_ \_ abilitata**. Per ulteriori informazioni sugli attributi di Active Directory disponibili, vedere [tutti gli attributi](/windows/desktop/ADSchema/attributes-all).

La tabella seguente elenca la regola di corrispondenza OID implementata da LDAP.



| OID regola di corrispondenza       | Identificatore di stringa (da Ntldap. h)   | Descrizione                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **\_bit della \_ regola di corrispondenza LDAP \_ \_ e**  | Viene trovata una corrispondenza solo se tutti i bit dall'attributo corrispondono al valore. Questa regola è equivalente a un operatore **and** bit per bit.                                                                  |
| 1.2.840.113556.1.4.804  | **\_bit della regola di corrispondenza LDAP \_ \_ \_ o**   | Viene trovata una corrispondenza se i bit dall'attributo corrispondono al valore. Questa regola è equivalente a un operatore **OR bit per** bit.                                                                        |
| 1.2.840.113556.1.4.1941 | **\_ \_ regola di corrispondenza LDAP \_ nella \_ catena** | Questa regola è limitata ai filtri applicati al DN. Si tratta di uno speciale operatore di corrispondenza "esteso" che percorre la catena di origini negli oggetti fino alla radice fino a quando non viene trovata una corrispondenza. |



 

La stringa di query di esempio seguente cerca gli oggetti gruppo per i quali è impostato il flag di **\_ \_ \_ sicurezza \_ abilitata per il tipo di gruppo ADS** . Tenere presente che per il valore di confronto viene usato il valore decimale della **\_ sicurezza del tipo di gruppo Ads \_ \_ \_ abilitata** (0x80000000 = 2147483648).


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



La **\_ regola di corrispondenza LDAP \_ \_ nella \_ catena** è un OID della regola di corrispondenza progettato per fornire un metodo per cercare l'origine di un oggetto. Molte applicazioni che usano Active Directory e AD LDS in genere funzionano con i dati gerarchici, ordinati in base alle relazioni padre-figlio. In precedenza, le applicazioni eseguivano un'espansione del gruppo transitiva per determinare l'appartenenza al gruppo, che usava troppa larghezza di banda di rete; le applicazioni devono creare più round trip per determinare se un oggetto è caduto "nella catena" Se un collegamento viene attraversato fino alla fine.

Un esempio di query di questo tipo è quello progettato per verificare se un utente "User1" è un membro del gruppo "group1". Impostare la base sul DN dell'utente `(cn=user1, cn=users, dc=x)` e l'ambito su `base` e usare la query seguente.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Analogamente, per trovare tutti i gruppi di cui "User1" è membro, impostare la base sul DN del contenitore gruppi; ad esempio `(OU=groupsOU, dc=x)` e l'ambito di `subtree` e usare il filtro seguente.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Si noti che quando si usa la **\_ \_ regola di corrispondenza LDAP \_ nella \_ catena**, l'ambito non è limitato, ovvero può essere `base` , `one-level` o `subtree` . Alcune query su sottoalberi potrebbero richiedere un maggior numero di processori, ad esempio la ricerca di collegamenti con un fan-out elevato; ovvero, elencando tutti i gruppi di cui un utente è membro. Le ricerche inefficienti registreranno i messaggi appropriati del registro eventi, come per qualsiasi altro tipo di query.

## <a name="wildcards"></a>Caratteri jolly

È anche possibile aggiungere caratteri jolly e Condizioni a un filtro di ricerca LDAP. Gli esempi seguenti illustrano le sottostringhe che possono essere usate per eseguire ricerche nella directory.

Ottenere tutte le voci:


```C++
(objectClass=*)
```



Ottenere le voci contenenti "Bob" in un punto qualsiasi nel nome comune:


```C++
(cn=*bob*)
```



Ottenere le voci con un nome comune maggiore o uguale a "Bob":


```C++
(cn>='bob')
```



Ottenere tutti gli utenti con un attributo di posta elettronica:


```C++
(&(objectClass=user)(email=*))
```



Ottenere tutte le voci utente con un attributo di posta elettronica e un cognome uguale a "Smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Ottenere tutte le voci utente con un nome comune che inizia con "Andy", "Steve" o "Margaret":


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Ottenere tutte le voci senza un attributo di posta elettronica:


```C++
(!(email=*))
```



La definizione formale del filtro di ricerca è la seguente (da [RFC 2254](https://tools.ietf.org/html/rfc2254)):


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



Il token &lt; attr &gt; è una stringa che rappresenta un attributeType. Il valore del token &lt; &gt; è una stringa che rappresenta un AttributeValue il cui formato è definito dal servizio directory sottostante.

Se un &lt; valore &gt; deve contenere il carattere asterisco ( \* ), parentesi aperta (() o parentesi destra ()), il carattere deve essere preceduto dal carattere di escape della barra rovesciata ( \\ ).

## <a name="special-characters"></a>Caratteri speciali

Se uno dei caratteri speciali seguenti deve essere visualizzato nel filtro di ricerca come valori letterali, è necessario sostituirli con la sequenza di escape elencata.



| Carattere ASCII | Sostituzione sequenza di escape |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28                       |
| )               | \\29                       |
| \\              | \\5C                       |
| NUL             | \\00                       |
| /               | \\2F                       |



 

> [!Note]  
> Nei casi in cui viene utilizzato un set di caratteri MultiByte, le sequenze di escape elencate in precedenza devono essere utilizzate se la ricerca viene eseguita da ADO con il sottolinguaggio SQL.

 

Inoltre, i dati binari arbitrari possono essere rappresentati usando la sintassi della sequenza di escape codificando ogni byte di dati binari con la barra rovesciata ( \\ ) seguita da due cifre esadecimali. Ad esempio, il valore a quattro byte 0x00000004 è codificato come \\ 00 00 \\ 00 \\ \\ 04 in una stringa di filtro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dialetto LDAP](ldap-dialect.md)
</dt> <dt>

[Sottolinguaggio SQL](sql-dialect.md)
</dt> <dt>

[Ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Ricerca con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
