---
description: Una voce di controllo di accesso condizionale (ACE) consente la valutazione di una condizione di accesso quando viene eseguito un controllo di accesso. Il linguaggio SDDL (Security Descriptor Definition Language) fornisce la sintassi per la definizione di Ace condizionali in un formato stringa.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Linguaggio di definizione del descrittore di sicurezza per le voci
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527013"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Linguaggio di definizione del descrittore di sicurezza per le voci

Una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale (ACE) consente la valutazione di una condizione di accesso quando viene eseguito un controllo di accesso. Il linguaggio SDDL (Security Descriptor Definition Language) fornisce la sintassi per la definizione di Ace condizionali in un formato stringa.

Il valore SDDL per una voce ACE condizionale è uguale a quello di qualsiasi voce ACE, con la sintassi per l'istruzione condizionale aggiunta alla fine della stringa ACE. Per informazioni su SDDL, vedere [Security Descriptor Definition Language](security-descriptor-definition-language.md).

Il \# segno "" è sinonimo di "0" negli attributi delle risorse. Ad esempio, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) equivale a e interpretato come D:ai (XA; OICI; fa;;; WD; (OctetStringType = = \# 01020300)).

-   [Formato stringa ACE condizionale](#conditional-ace-string-format)
-   [Espressioni condizionali](#conditional-expressions)
-   [Attributes (Attributi)](#attributes)
-   [Operatori](#operators)
-   [Ordine di precedenza degli operatori](#operator-precedence)
-   [Valori sconosciuti](#unknown-values)
-   [Valutazione ACE condizionale](#conditional-ace-evaluation)
-   [esempi](#examples)
-   [Argomenti correlati](#related-topics)

## <a name="conditional-ace-string-format"></a>Formato stringa ACE condizionale

Ogni voce ACE in una stringa del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) è racchiusa tra parentesi. I campi della voce ACE sono nell'ordine seguente e sono separati da punti e virgola (;).

*AceType ***;** _AceFlags_* _;_ *_Diritti_*_;_ *_ObjectGUID_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

I campi sono descritti in [stringhe ACE](ace-strings.md), con le eccezioni seguenti.

-   Il campo *AceType* può essere una delle stringhe seguenti.

    | Stringa di tipo ACE | Costante in SDDL. h                         | Valore AceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | XA<br/> | \_accesso callback \_ SDDL \_ consentito<br/> | \_ \_ tipo ACE di callback consentito \_ per \_ l'accesso<br/> |
    | XD<br/> | \_accesso callback \_ SDDL \_ negato<br/>  | \_ \_ tipo ACE di callback accesso negato \_ \_<br/>  |

    

     

-   Nella stringa ACE sono incluse una o più espressioni condizionali, racchiuse tra parentesi alla fine della stringa.

## <a name="conditional-expressions"></a>Espressioni condizionali

Un'espressione condizionale può includere uno qualsiasi degli elementi seguenti.



| Elemento dell'espressione                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Verifica se l'attributo specificato ha un valore diverso da zero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Exists** *attributeName*<br/>                             | Verifica se l'attributo specificato esiste nel contesto client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valore* dell' *operatore* *attributeName*<br/>                     | Restituisce il risultato dell'operazione specificata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| * ConditionalExpression * **\|\|** _ConditionalExpression_<br/> | Verifica se una delle espressioni condizionali specificate è true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Verifica se entrambe le espressioni condizionali specificate sono true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Inverso di un'espressione condizionale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Membro \_ di {**_SidArray_*_}_*<br/>                         | Verifica se la matrice di [**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) del contesto client contiene tutti gli [ID di sicurezza](security-identifiers.md) (SID) nell'elenco delimitato da virgole specificato da *SidArray*.<br/> Per le voci ACE Consenti, un SID del contesto client deve avere l'attributo **\_ \_ Enabled del gruppo se** impostato per essere considerato una corrispondenza.<br/> Per le voci ACE di negazione, un SID del contesto client deve avere il **\_ gruppo se \_ abilitato** oppure il **\_ gruppo se usa solo l'attributo \_ \_ \_ Deny \_ solo per** essere considerato corrispondente.<br/> La matrice *SidArray* può contenere stringhe SID (ad esempio, "S-1-5-6") o alias SID (ad esempio, "BA"<br/> |



 

## <a name="attributes"></a>Attributi

Un attributo rappresenta un elemento nella matrice [**di \_ \_ \_ informazioni sugli attributi di sicurezza AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) nel contesto client. Un nome di attributo può contenere tutti i caratteri alfanumerici e i caratteri ":", "/", "." e " \_ ".

Un valore di attributo può essere uno dei seguenti tipi.



| Tipo di valore         | Descrizione                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer<br/> | Intero a 64 bit nella notazione decimale o esadecimale.<br/>                                                                                                                              |
| string<br/>  | Valore stringa delimitato da virgolette.<br/>                                                                                                                                                      |
| SID<br/>     | SID (S-1-1-0) o SID (BA). Deve essere in RHS del membro \_ del membro o del \_ dispositivo \_ di.<br/>                                                                                                           |
| BLOB<br/>    | \# seguito da numeri esadecimali. Se la lunghezza dei numeri è dispari, l'oggetto \# viene convertito in 0 per renderlo uniforme. Inoltre, un oggetto \# visualizzato altrove nel valore viene convertito in 0.<br/> |



 

## <a name="operators"></a>Operatori

Gli operatori seguenti sono definiti per l'utilizzo nelle espressioni condizionali per verificare i valori degli attributi. Tutti questi sono operatori binari e usati nel *valore* dell' *operatore* form *attributeName* .



| Operatore            | Descrizione                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Definizione convenzionale.<br/>                                                                                      |
| !=<br/>       | Definizione convenzionale.<br/>                                                                                      |
| <<br/>     | Definizione convenzionale.<br/>                                                                                      |
| <=<br/>    | Definizione convenzionale.<br/>                                                                                      |
| ><br/>     | Definizione convenzionale.<br/>                                                                                      |
| >=<br/>    | Definizione convenzionale.<br/>                                                                                      |
| Contiene<br/> | **True** se il valore dell'attributo specificato è un superset del valore specificato. in caso contrario, **false**.<br/>  |
| Qualsiasi \_<br/>  | **True** se il valore specificato è un superset del valore dell'attributo specificato. in caso contrario, **false**. <br/> |



 

Inoltre, gli operatori unari esistono, il membro \_ di e la negazione (!) sono definiti come descritto nella tabella espressioni condizionali.

L'operatore "Contains" deve essere preceduto e seguito da uno spazio vuoto e l'operatore "Any \_ of" deve essere preceduto da uno spazio vuoto.

## <a name="operator-precedence"></a>Ordine di precedenza degli operatori

Gli operatori vengono valutati nell'ordine di precedenza seguente, in cui le operazioni di uguale precedenza vengono valutate da sinistra a destra.

1.  Exists, membro \_ di
2.  Contiene \_ , qualsiasi
3.  = =,! =, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Inoltre, qualsiasi parte di un'espressione condizionale può essere racchiusa tra parentesi. Le espressioni racchiuse tra parentesi vengono valutate per prime.

## <a name="unknown-values"></a>Valori sconosciuti

I risultati delle espressioni condizionali restituiscono talvolta un valore **sconosciuto**. Ad esempio, una qualsiasi delle operazioni relazionali restituisce **Unknown** quando l'attributo specificato non esiste.

Nella tabella seguente vengono descritti i risultati di un'operazione **and** logica tra due espressioni condizionali, *ConditionalExpression1* e *ConditionalExpression2*.



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



 

Nella tabella seguente vengono descritti i risultati di un'operazione **or** logica tra due espressioni condizionali, *ConditionalExpression1* e *ConditionalExpression2*.



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



 

Anche la negazione di un'espressione condizionale con un valore **sconosciuto** è **sconosciuta**.

## <a name="conditional-ace-evaluation"></a>Valutazione ACE condizionale

La tabella seguente descrive il risultato del controllo di accesso di una voce ACE condizionale a seconda della valutazione finale dell'espressione condizionale.

| Tipo ACE         | true             | FALSE                 | UNKNOWN               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | Ignora ACE<br/> | Ignora ACE<br/> |
| Nega<br/>  | Nega<br/>  | Ignora ACE<br/> | Nega<br/>       |



 

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato il modo in cui i criteri di accesso specificati sono rappresentati da una voce ACE condizionale definita mediante SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica
</dt> <dd>

Consenti Esegui a tutti se sono soddisfatte entrambe le condizioni seguenti:

-   Titolo = PM
-   Divisione = Finance o Division = Sales

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica
</dt> <dd>

Consenti Esegui se uno dei progetti utente si interseca con i progetti del file.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Project Qualsiasi \_ @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politica
</dt> <dd>

Consenti l'accesso in lettura se l'utente ha eseguito l'accesso con una smart card, è un operatore di backup e si connette da un computer con BitLocker abilitato.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FR;;; S-1-1-0; (Membro \_ di {SID (SID smart card \_ ), SID (BO)}  && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

