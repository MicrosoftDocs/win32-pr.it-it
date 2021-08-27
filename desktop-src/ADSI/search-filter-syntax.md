---
title: Sintassi del filtro di ricerca
description: I filtri di ricerca consentono di definire i criteri di ricerca e di fornire ricerche più efficienti ed efficaci.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Sintassi del filtro di ricerca ADSI
- query, sintassi del filtro di ricerca
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 9ea6b347da1c840ef6bd1dd32bb32f96e7be86dfb93e6c1e71cdbb06bd52ba97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005491"
---
# <a name="search-filter-syntax"></a>Sintassi del filtro di ricerca

I filtri di ricerca consentono di definire i criteri di ricerca e di fornire ricerche più efficienti ed efficaci.

ADSI supporta i filtri di ricerca LDAP definiti in RFC2254. Questi filtri di ricerca sono rappresentati da stringhe Unicode. La tabella seguente elenca alcuni esempi di filtri di ricerca LDAP.



| Filtro di ricerca                                                               | Descrizione                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass= \* )"                                                          | Tutti gli oggetti .                                               |
| "(&(objectCategory=person)(objectClass=user)(!( cn=andy))                  | Tutti gli oggetti utente, ad esempio "andy".                               |
| "(sn=sm \* )"                                                                 | Tutti gli oggetti con un cognome che inizia con "sm".          |
| "(&(objectCategory=person)(objectClass=contact)( \| (sn=Smith)(sn=ObjectCategory))))" | Tutti i contatti con cognome uguale a "Smith" o "Smith". |



 

Questi filtri di ricerca usano uno dei formati seguenti.


```C++
<filter>=(<attribute><operator><value>)
```



oppure


```C++
(<operator><filter1><filter2>)
```



I filtri di ricerca ADSI vengono usati in due modi. Fanno parte del dialetto LDAP per l'invio di query tramite OLE DB provider. Vengono usati anche con [**l'interfaccia IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

## <a name="operators"></a>Operatori

Nella tabella seguente sono elencati gli operatori di filtro di ricerca usati di frequente.



| Operatore logico | Descrizione                                |
|------------------|--------------------------------------------|
| =                | Uguale a                                   |
| ~=               | Approssimativamente uguale a                     |
| <=            | Lessicograficamente minore o uguale a    |
| >=            | Lessicograficamente maggiore o uguale a |
| &                | AND                                        |
| \|               | OR                                         |
| !                | NOT                                        |



 

Oltre agli operatori precedenti, LDAP definisce due identificatori di oggetto regola (OID) corrispondenti che possono essere usati per eseguire confronti bit per bit di valori numerici. Le regole di corrispondenza hanno la sintassi seguente.


```C++
<attribute name>:<matching rule OID>:=<value>
```



" attribute name " è il &lt; &gt; valore **lDAPDisplayName** dell'attributo, " rule OID " è l'OID per la regola di corrispondenza e " value " è il valore da usare per &lt; il &gt; &lt; &gt; confronto. Tenere presente che non è possibile usare spazi in questa stringa. " value " deve essere un numero decimale. Non può essere un numero esadecimale o un nome costante, ad esempio &lt; &gt; **ADS \_ GROUP TYPE \_ SECURITY \_ \_ ENABLED.** Per altre informazioni sugli attributi di Active Directory disponibili, vedere [Tutti gli attributi.](/windows/desktop/ADSchema/attributes-all)

Nella tabella seguente sono elencati gli OID delle regole di corrispondenza implementati da LDAP.



| OID regola di corrispondenza       | Identificatore di stringa (da Ntldap.h)   | Descrizione                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **BIT E \_ DELLA \_ REGOLA DI CORRISPONDENZA \_ LDAP \_**  | Viene trovata una corrispondenza solo se tutti i bit dell'attributo corrispondono al valore. Questa regola equivale a un operatore **AND** bit per bit.                                                                  |
| 1.2.840.113556.1.4.804  | **BIT \_ DELLA REGOLA DI CORRISPONDENZA LDAP \_ \_ \_ O**   | Se i bit dell'attributo corrispondono al valore, viene trovata una corrispondenza. Questa regola equivale a un operatore **OR** bit per bit.                                                                        |
| 1.2.840.113556.1.4.1941 | **REGOLA \_ DI CORRISPONDENZA LDAP NELLA \_ \_ \_ CATENA** | Questa regola è limitata ai filtri che si applicano al DN. Si tratta di uno speciale operatore di corrispondenza "esteso" che consente di raggiungere la radice fino alla radice fino a trovare una corrispondenza. |



 

La stringa di query di esempio seguente cerca gli oggetti gruppo per cui è impostato il flag **ADS \_ GROUP TYPE \_ SECURITY \_ \_ ENABLED.** Tenere presente che per il valore di confronto viene usato il valore decimale **di ADS \_ GROUP TYPE \_ SECURITY \_ \_ ENABLED** (0x80000000 = 2147483648).


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



LDAP **\_ MATCHING RULE IN \_ CHAIN \_ \_ è** un OID della regola di corrispondenza progettato per fornire un metodo per cercare l'origine di un oggetto. Molte applicazioni che usano AD e AD LDS in genere funzionano con dati gerarchici, ordinati in base alle relazioni padre-figlio. In precedenza, le applicazioni hanno eseguito l'espansione transitiva dei gruppi per determinare l'appartenenza ai gruppi, che usava una larghezza di banda di rete troppo elevata. le applicazioni dovevano eseguire più roundtrip per determinare se un oggetto era "nella catena" se un collegamento viene attraversato fino alla fine.

Un esempio di query di questo tipo è una query progettata per verificare se un utente "user1" è membro del gruppo "group1". Impostare la base sul DN dell'utente `(cn=user1, cn=users, dc=x)` e l'ambito su `base` e usare la query seguente.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



Analogamente, per trovare tutti i gruppi di cui "user1" è membro, impostare la base sul DN del contenitore groups; ad esempio `(OU=groupsOU, dc=x)` e l'ambito su `subtree` e usare il filtro seguente.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Si noti che quando si **usa LDAP MATCHING RULE IN \_ \_ \_ \_ CHAIN,** l'ambito non è limitato: può essere `base` , o `one-level` `subtree` . Alcune di queste query sui sottoalberi possono richiedere un utilizzo più intensivo del processore, ad esempio la ricerca di collegamenti con un fan-out elevato; ad esempio elencando tutti i gruppi di cui un utente è membro. Ricerche inefficienti registrano messaggi del registro eventi appropriati, come per qualsiasi altro tipo di query.

## <a name="wildcards"></a>Caratteri jolly

È anche possibile aggiungere caratteri jolly e condizioni a un filtro di ricerca LDAP. Negli esempi seguenti vengono mostrate sottostringhe che possono essere usate per eseguire ricerche nella directory.

Ottenere tutte le voci:


```C++
(objectClass=*)
```



Ottenere le voci contenenti "bob" in un punto qualsiasi nel nome comune:


```C++
(cn=*bob*)
```



Ottenere le voci con un nome comune maggiore o uguale a "bob":


```C++
(cn>='bob')
```



Ottenere tutti gli utenti con un attributo di posta elettronica:


```C++
(&(objectClass=user)(email=*))
```



Ottenere tutte le voci utente con un attributo email e un cognome uguale a "smith":


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Ottenere tutte le voci utente con un nome comune che inizia con "andy", "steve" o "più":


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Ottenere tutte le voci senza un attributo email:


```C++
(!(email=*))
```



La definizione formale del filtro di ricerca è la seguente [(da RFC 2254):](https://tools.ietf.org/html/rfc2254)


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



&lt;L'attr &gt; del token è una stringa che rappresenta un AttributeType. Il valore &lt; del token è una stringa che rappresenta un AttributeValue il cui formato è definito dal servizio directory &gt; sottostante.

Se un valore deve contenere il carattere asterisco ( ), parentesi aperta (() ) o parentesi destra (), il carattere deve essere preceduto dal carattere di escape barra &lt; &gt; \* rovesciata ( \\ ).

## <a name="special-characters"></a>Caratteri speciali

Se uno dei caratteri speciali seguenti deve essere visualizzato nel filtro di ricerca come valori letterali, deve essere sostituito dalla sequenza di escape elencata.



| Carattere ASCII | Sostituzione della sequenza di escape |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28                       |
| )               | \\29                       |
| \\              | \\5c                       |
| NUL             | \\00                       |
| /               | \\2f                       |



 

> [!Note]  
> Nei casi in cui viene usato un set di caratteri multibyte, è necessario usare le sequenze di escape elencate in precedenza se la ricerca viene eseguita da ADO con il SQL specificato.

 

Inoltre, i dati binari arbitrari possono essere rappresentati usando la sintassi della sequenza di escape codificando ogni byte di dati binari con la barra rovesciata ( ) seguita da due cifre \\ esadecimali. Ad esempio, il valore a quattro byte 0x00000004 codificato come \\ 00 \\ 00 \\ 00 \\ 04 in una stringa di filtro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dialetto LDAP](ldap-dialect.md)
</dt> <dt>

[SQL dialetto](sql-dialect.md)
</dt> <dt>

[Ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Ricerca con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
