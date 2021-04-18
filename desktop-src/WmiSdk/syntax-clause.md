---
description: Contiene una clausola della sintassi che definisce i dati e il tipo per l'oggetto MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Clausola SYNTAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318856"
---
# <a name="syntax-clause"></a>Clausola SYNTAX

La macro di [tipo oggetto](object-type-macro.md) contiene una clausola della sintassi che definisce i dati e il tipo per l'oggetto MIB. Sebbene il provider SNMP osservi le regole generali per il mapping delle clausole di sintassi, il provider segue anche le regole specifiche di diversi tipi di dati.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Le regole di mapping seguenti si applicano a tutti i tipi di dati descritti nella tabella seguente:

-   La rappresentazione testuale della clausola della sintassi è mappata alla **\_ convenzione testuale** del qualificatore della proprietà CIM.
-   La definizione del tipo denominato nella clausola della sintassi è mappata alla **\_ sintassi dell'oggetto** qualificatore della proprietà CIM. Questo mapping è diverso a seconda del tipo di dati. Per ulteriori informazioni, vedere le descrizioni del mapping.
-   Il tipo SNMP usato per la codifica dei frame del protocollo SNMPv1 e SNMPv2C è mappato alla **codifica** del qualificatore della proprietà CIM.
-   Il qualificatore di proprietà CIM **CimType** contiene la rappresentazione testuale che formatta il valore del protocollo CIM sottostante.

Nella tabella seguente sono elencati i tipi di dati con regole specifiche che regolano il comportamento di mapping del provider.



| Tipo di dati SNMP                                     | Descrizione                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipo primitivo](#primitive-type)                  | Uno dei tipi di dati di base definiti nella struttura delle informazioni di gestione (SMI) Documents RFC 1213 e RFC 1903.                                                                                                                            |
| [Convenzione testuale](textual-convention-macro.md) | Definizione del tipo generata tramite l'utilizzo esplicito della macro della **convenzione testuale** SNMPv2c o generata tramite l'utilizzo di un tipo denominato. Una convenzione testuale assegna un nome e, in alcuni casi, un intervallo di valori a un tipo di dati esistente. |
| [Tipo denominato](#named-type)                          | Riferimento denominato a un tipo primitivo, una convenzione testuale o un tipo vincolato.                                                                                                                                                                    |
| [Tipo vincolato](#constrained-type)              | Il tipo primitivo, il tipo denominato o la convenzione testuale che è stato vincolato da un meccanismo di subtipizzazione definito nei documenti SMI RFC 1213 e RFC 1903.                                                                                      |



 

## <a name="primitive-type"></a>Tipo primitivo

Il tipo primitivo è uno dei tipi di dati di base definiti nella struttura delle informazioni di gestione (SMI) documenti RFC 1213 e RFC 1903. I tipi primitivi SNMP sono mappati ai tipi definiti CIM. La tabella seguente elenca il mapping che si verifica quando la clausola della sintassi fa riferimento in modo esplicito a un tipo primitivo per SNMPv1. I qualificatori della **\_ convenzione testuale**, della **codifica** e della **\_ sintassi dell'oggetto** sono sempre uguali al tipo MIB e il valore predefinito è sempre **null**.



| Tipo MIB         | Tipo Variant CIM | valore CimType |
|------------------|------------------|---------------|
| INTEGER          | VT \_ I4           | **sint32**    |
| OCTETSTRING      | \_BSTR VT         | **string**    |
| OBJECTIDENTIFIER | \_BSTR VT         | **string**    |
| NULL             | VT \_ null         | Non supportato |
| IpAddress        | \_BSTR VT         | **string**    |
| Contatore          | VT \_ I4           | **uint32**    |
| Misuratore            | VT \_ I4           | **uint32**    |
| TimeTicks        | VT \_ I4           | **uint32**    |
| Opaco           | \_BSTR VT         | **string**    |
| NetworkAddress   | \_BSTR VT         | **string**    |



 

Il provider ignora la macro del tipo di oggetto quando la clausola della sintassi fa riferimento a **null**, in modo esplicito o tramite un'assegnazione di tipo denominata. La tabella seguente elenca il mapping che si verifica quando la clausola della sintassi fa riferimento in modo esplicito a un tipo primitivo per SNMPv2. I qualificatori della **\_ convenzione testuale**, della **codifica** e della **\_ sintassi dell'oggetto** sono sempre uguali al tipo MIB e il valore predefinito è sempre **null**.



| Tipo MIB          | Tipo Variant CIM | valore CimType |
|-------------------|------------------|---------------|
| INTEGER           | VT \_ I4           | **sint32**    |
| STRINGA OTTETTO      | \_BSTR VT         | **string**    |
| IDENTIFICATORE OGGETTO | \_BSTR VT         | **string**    |
| IpAddress         | \_BSTR VT         | **string**    |
| Counter32         | VT \_ I4           | **uint32**    |
| Gauge32           | VT \_ I4           | **uint32**    |
| Unsigned32        | VT \_ I4           | **uint32**    |
| Integer32         | VT \_ I4           | **sint32**    |
| Counter64         | \_BSTR VT         | **uint64**    |
| TimeTicks         | VT \_ I4           | **uint32**    |
| Opaco            | \_BSTR VT         | **string**    |



 

## <a name="named-type"></a>Tipo denominato

I tipi denominati SNMP vengono mappati ai tipi definiti CIM. Quando la clausola della sintassi fa riferimento a un [tipo primitivo](#primitive-type), a una [convenzione testuale](textual-convention-macro.md)o a un [tipo vincolato](#constrained-type) tramite una derivazione di assegnazione del tipo, utilizzare tali tipi per determinare quali procedure di mapping applicare.

-   Se, tramite la derivazione delle regole di assegnazione del tipo, si verifica una definizione di tipo vincolato:

    -   Se, tramite un'ulteriore derivazione, si verifica una delle convenzioni testuali elencate nella [macro della convenzione testuale](textual-convention-macro.md), applicare le regole di mapping per i tipi vincolati e le convenzioni testuali.
    -   In caso contrario, se si riscontra uno dei tipi primitivi elencati in una tabella di tipi primitivi, applicare le regole di mapping per i tipi primitivi e i tipi vincolati.

-   Se si verifica una delle convenzioni testuali elencate nella [ \_ macro della convenzione testuale](textual-convention-macro.md), applicare le regole di mapping per le convenzioni testuali.
-   Se si riscontra uno dei tipi primitivi elencati in una tabella di tipo primitiva, applicare le regole di mapping per i tipi primitivi.

> [!Note]  
> Le classi che contengono tipi di proprietà che non sono conformi al mapping descritto in precedenza non sono valide. In questo caso, il provider restituisce un errore se e quando il provider richiede il recupero di una definizione di classe durante l'esecuzione di una funzione di recupero dell'istanza.

 

## <a name="constrained-type"></a>Tipo vincolato

Un tipo vincolato è un tipo primitivo, un tipo denominato o una convenzione testuale che è stata vincolata da un meccanismo di sottotipizzazione definito nei documenti SMI RFC 1213 e RFC 1903. Quando si verifica la sottotipizzazione, per specificare i valori dei sottotipi sono necessari qualificatori CIM aggiuntivi. La definizione del tipo denominato nella clausola della sintassi esegue il mapping Verbatim alla sintassi dell' **oggetto \_** qualificatore della proprietà CIM fino a, ma non include i vincoli del sottotipo.

I sottotipi possono seguire uno dei formati seguenti:

-   INTEGER enumerato

    L' **enumerazione** CIM Property Qualifier specifica i valori enumerati. Questo qualificatore è rappresentato come stringa contenente un elenco delimitato da virgole di valori interi con segno a 32 bit. Nella tabella seguente sono elencati i tipi di mapping. Il valore predefinito è sempre **null**.



| Tipo MIB vincolato | Tipo Variant CIM | Qualificatori CIM                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| INTEGER enumerato   | \_BSTR VT         | **\_ convenzione testuale**: enumeratedinteger<br/> **codifica**: integer<br/> **CimType**: stringa<br/> |



 

-   BITS

    I **bit** del qualificatore della proprietà CIM specificano i valori enumerati. Questo qualificatore è rappresentato come stringa contenente un elenco delimitato da virgole di valori interi con segno a 32 bit. Nella tabella seguente sono elencati i tipi di mapping. Il valore predefinito è sempre **null**.



| Tipo MIB vincolato | Tipo Variant CIM      | Qualificatori CIM                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | \_ \| VT BSTR matrice \_ VT | **\_ convenzione testuale**: BITS<br/> **codifica**: OCTETSTRING<br/> **CimType**: stringa<br/> |



 

-   A lunghezza variabile

    Quando la clausola della sintassi fa riferimento a un tipo primitivo, a un tipo denominato o a una convenzione testuale sottoposta a una stringa di ottetto a lunghezza variabile o opaca, la **\_ lunghezza variabile** del qualificatore di proprietà CIM specifica i valori minimo, massimo e a lunghezza fissa associati alla definizione del tipo. Questo qualificatore viene implementato come stringa nel formato seguente, in cui i valori a lunghezza variabile sono rappresentati come interi senza segno a 32 bit.

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   A lunghezza fissa

    Quando la clausola della sintassi fa riferimento a un tipo primitivo, a un tipo denominato o a una convenzione testuale sottoposta a una stringa di ottetto a lunghezza fissa o opaca, la **\_ lunghezza fissa** del qualificatore di proprietà CIM specifica il valore a lunghezza fissa. Questo qualificatore è rappresentato come valore intero senza segno a 32 bit.

-   Range

    Quando la clausola della sintassi fa riferimento a un tipo primitivo, a un tipo denominato o a una convenzione testuale sottoposta a un numero intero o a un misuratore a valore fisso o a intervalli, il **\_ valore della variabile** del qualificatore della proprietà CIM specifica i valori a intervalli e fissi associati alla definizione del tipo. Questo qualificatore viene implementato come stringa nel formato seguente, in cui i valori di intervallo e di lunghezza fissa sono rappresentati come interi senza segno a 32 bit.

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>Codice di esempio

Nell'esempio seguente viene descritto un sottotipo INTEGER enumerato.

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

Questo esempio esegue il mapping a:

``` syntax
enumeration("up(1),down(2),testing(3)")
```

Nell'esempio di codice riportato di seguito viene descritto un sottotipo BITS.

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

Nell'esempio di codice seguente viene eseguito il mapping a:

``` syntax
bits("up(1),down(2),testing(3)")
```

Nell'esempio di codice riportato di seguito viene descritto un sottotipo a lunghezza variabile.

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

Questo esempio esegue il mapping a:

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

Nell'esempio seguente viene descritto un sottotipo a lunghezza fissa.

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

Questo esempio esegue il mapping a:

``` syntax
fixed_length(6)
```

Nell'esempio seguente viene descritto un sottotipo di intervallo.

``` syntax
Status := INTEGER (10..20|8)
```

Questo esempio esegue il mapping a:

``` syntax
variable_value("10..20,8")
```

 

 




