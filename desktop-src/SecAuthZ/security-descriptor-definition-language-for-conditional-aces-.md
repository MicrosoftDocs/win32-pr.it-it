---
description: Una voce di controllo di accesso condizionale consente di valutare una condizione di accesso quando viene eseguito un controllo di accesso. Il linguaggio SDDL (Security Descriptor Definition Language) fornisce la sintassi per la definizione di ACE condizionali in formato stringa.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Linguaggio di definizione del descrittore di sicurezza per ACE condizionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0a746460c7582d95e0c95e2a2c179aac2eb29456418234cb52e842c8c56738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780526"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Linguaggio di definizione del descrittore di sicurezza per ACE condizionali

Una voce [*di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale consente di valutare una condizione di accesso quando viene eseguito un controllo di accesso. Il linguaggio SDDL (Security Descriptor Definition Language) fornisce la sintassi per la definizione di ACE condizionali in formato stringa.

Il linguaggio SDDL per una ACE condizionale è lo stesso di qualsiasi ACE, con la sintassi per l'istruzione condizionale aggiunta alla fine della stringa ACE. Per informazioni su SDDL, vedere [Security Descriptor Definition Language.](security-descriptor-definition-language.md)

Il segno \# " " è sinonimo di "0" negli attributi della risorsa. Ad esempio, D:AI(XA;OICI;FA;;; WD;(OctetStringType== 1 2 3 )) è equivalente e interpretato \# \# come \# \# \# D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 01020300)).

-   [Formato stringa ACE condizionale](#conditional-ace-string-format)
-   [Espressioni condizionali](#conditional-expressions)
-   [Attributes (Attributi)](#attributes)
-   [Operatori](#operators)
-   [Precedenza degli operatori](#operator-precedence)
-   [Valori sconosciuti](#unknown-values)
-   [Valutazione ACE condizionale](#conditional-ace-evaluation)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="conditional-ace-string-format"></a>Formato stringa ACE condizionale

Ogni ACE in una [*stringa del descrittore di*](/windows/desktop/SecGloss/s-gly) sicurezza è racchiusa tra parentesi. I campi della ACE sono nell'ordine seguente e sono separati da punti e virgola (;).

*AceType***;** _AceFlags_* _;_ *_Diritti_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

I campi sono descritti in [Stringhe ACE,](ace-strings.md)con le eccezioni seguenti.

-   Il *campo AceType* può essere una delle stringhe seguenti.

    | Stringa di tipo ACE | Costante in Sddl.h                         | Valore AceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | "XA"<br/> | ACCESSO DI CALLBACK SDDL \_ \_ \_ CONSENTITO<br/> | ACCESS \_ ALLOWED \_ CALLBACK \_ ACE \_ TYPE<br/> |
    | "XD"<br/> | ACCESSO CALLBACK SDDL \_ \_ \_ NEGATO<br/>  | TIPO \_ \_ ACE CALLBACK \_ DI ACCESSO \_ NEGATO<br/>  |

    

     

-   La stringa ACE include una o più espressioni condizionali, racchiuse tra parentesi alla fine della stringa.

## <a name="conditional-expressions"></a>Espressioni condizionali

Un'espressione condizionale può includere uno degli elementi seguenti.



| Elemento dell'espressione                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Verifica se l'attributo specificato ha un valore diverso da zero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **exists** *AttributeName*<br/>                             | Verifica se l'attributo specificato esiste nel contesto client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valore dell'operatore*  *AttributeName*<br/>                     | Restituisce il risultato dell'operazione specificata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *ConditionalExpression* **\|\|** _ConditionalExpression_<br/> | Verifica se una delle espressioni condizionali specificate è true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Verifica se entrambe le espressioni condizionali specificate sono true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Inverso di un'espressione condizionale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Membro \_ di{**_SidArray_*_}_*<br/>                         | Verifica se la [**matrice SID \_ E \_ ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) del contesto client contiene tutti gli ID di sicurezza (SID) nell'elenco delimitato da virgole specificato da *SidArray.* [](security-identifiers.md)<br/> Per consentire ACE, un SID del contesto client deve avere **\_ l edizione Standard'attributo GROUP \_ ENABLED** impostato per essere considerato una corrispondenza.<br/> Per gli ACE Deny, un SID del contesto client deve avere l'attributo **edizione Standard \_ GROUP \_ ENABLED** o **l'attributo edizione Standard GROUP USE FOR DENY \_ \_ \_ \_ \_ ONLY** impostato per essere considerato una corrispondenza.<br/> La *matrice SidArray* può contenere stringhe SID (ad esempio, "S-1-5-6") o alias SID (ad esempio, "BA"<br/> |



 

## <a name="attributes"></a>Attributi

Un attributo rappresenta un elemento nella matrice [**AUTHZ \_ SECURITY \_ ATTRIBUTES \_ INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) nel contesto client. Un nome di attributo può contenere qualsiasi carattere alfanumerico e qualsiasi carattere ":", "/", "." e " \_ ".

Un valore di attributo può essere uno dei tipi seguenti.



| Tipo di valore         | Descrizione                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intero<br/> | Intero a 64 bit in notazione decimale o esadecimale.<br/>                                                                                                                              |
| string<br/>  | Valore stringa delimitato da virgolette.<br/>                                                                                                                                                      |
| SID<br/>     | SID(S-1-1-0) o SID (BA). Deve essere in RHS membro \_ di o membro del dispositivo \_ \_ di.<br/>                                                                                                           |
| BLOB<br/>    | \# seguito da numeri esadecimali. Se la lunghezza dei numeri è dispari, viene \# convertito in 0 per renderlo pari. Un oggetto \# visualizzato altrove nel valore viene convertito in 0.<br/> |



 

## <a name="operators"></a>Operatori

Gli operatori seguenti sono definiti per l'uso nelle espressioni condizionali per testare i valori degli attributi. Tutti questi operatori sono operatori binari e vengono usati nel formato *Valore dell'operatore AttributeName*  *.*



| Operatore            | Descrizione                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Definizione convenzionale.<br/>                                                                                      |
| !=<br/>       | Definizione convenzionale.<br/>                                                                                      |
| <<br/>     | Definizione convenzionale.<br/>                                                                                      |
| <=<br/>    | Definizione convenzionale.<br/>                                                                                      |
| ><br/>     | Definizione convenzionale.<br/>                                                                                      |
| >=<br/>    | Definizione convenzionale.<br/>                                                                                      |
| Contiene<br/> | **TRUE** se il valore dell'attributo specificato è un superset del valore specificato. in caso contrario, **FALSE.**<br/>  |
| Uno \_ qualsiasi dei<br/>  | **TRUE** se il valore specificato è un superset del valore dell'attributo specificato; in caso contrario, **FALSE.** <br/> |



 

Inoltre, gli operatori unari Exists, Member of e negation (!) sono definiti come \_ descritto nella tabella Espressioni condizionali.

L'operatore "Contains" deve essere preceduto e seguito da spazi vuoti e l'operatore "Any of" deve \_ essere preceduto da uno spazio vuoto.

## <a name="operator-precedence"></a>Ordine di precedenza degli operatori

Gli operatori vengono valutati nell'ordine di precedenza seguente, con le operazioni con uguale precedenza valutate da sinistra a destra.

1.  Exists, Membro \_ di
2.  Contains, Any \_ of
3.  ==, !=, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Inoltre, qualsiasi parte di un'espressione condizionale può essere racchiusa tra parentesi. Le espressioni tra parentesi vengono valutate per prime.

## <a name="unknown-values"></a>Valori sconosciuti

I risultati delle espressioni condizionali talvolta restituiscono un valore **Unknown.** Ad esempio, una delle operazioni relazionali restituisce **Unknown** quando l'attributo specificato non esiste.

Nella tabella seguente vengono descritti i risultati di un'operazione **AND** logica tra due espressioni condizionali, *ConditionalExpression1* *e ConditionalExpression2.*



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **&&** *ConditionalExpression2* |
|--------------------------|--------------------------|----------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                      |
| **TRUE**<br/>      | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |
| **FALSE**<br/>     | **TRUE**<br/>      | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **UNKNOWN**<br/>                                   |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |



 

Nella tabella seguente vengono descritti i risultati di **un'operazione OR** logica tra due espressioni condizionali, *ConditionalExpression1* *e ConditionalExpression2.*



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **\|\|** *ConditionalExpression2* |
|--------------------------|--------------------------|------------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **FALSE**<br/>     | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                       |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |



 

Anche la negazione di un'espressione condizionale con valore **UNKNOWN** è **UNKNOWN.**

## <a name="conditional-ace-evaluation"></a>Valutazione ACE condizionale

Nella tabella seguente viene descritto il risultato del controllo di accesso di una ACE condizionale a seconda della valutazione finale dell'espressione condizionale.

| Tipo ACE         | true             | FALSE                 | UNKNOWN               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | Ignora ACE<br/> | Ignora ACE<br/> |
| Nega<br/>  | Nega<br/>  | Ignora ACE<br/> | Nega<br/>       |



 

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato come i criteri di accesso specificati sono rappresentati da una ACE condizionale definita tramite SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica
</dt> <dd>

Consenti l'esecuzione a tutti se vengono soddisfatte entrambe le condizioni seguenti:

-   Titolo = PM
-   Divisione = Finanza o Divisione = Vendite

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Title =="PM" && ( @User.Division =="Finance" \| \| @User.Division ==" Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica
</dt> <dd>

Consentire l'esecuzione se uno dei progetti dell'utente si interseca con i progetti di file.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Project Qualsiasi \_ di @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica
</dt> <dd>

Consentire l'accesso in lettura se l'utente ha eseguito l'accesso con un smart card, è un operatore di backup e si connette da un computer con Bitlocker abilitato.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ;FR;;; S-1-1-0; (Membro \_ di {SID(SID smart \_ card), SID(BO)} && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\[MS-DTYP: \] Linguaggio di descrizione del descrittore di sicurezza](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

