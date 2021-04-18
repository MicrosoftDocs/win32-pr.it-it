---
description: Le convenzioni testuali SNMP sono mappate ai tipi definiti CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro convenzione testuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309765"
---
# <a name="textual-convention-macro"></a>Macro convenzione testuale

Le convenzioni testuali SNMP sono mappate ai tipi definiti CIM.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Le regole di mapping seguenti si applicano alle convenzioni testuali SNMP:

-   La definizione del tipo denominato nella clausola della sintassi esegue il mapping Verbatim alla **\_ sintassi dell'oggetto** qualificatore della proprietà CIM.
-   Usare la tabella seguente per eseguire il mapping delle convenzioni testuali quando la clausola della sintassi fa riferimento in modo esplicito a una convenzione testuale di una macro della convenzione testuale SNMPv2C o fa riferimento a una convenzione testuale implicita. Il valore predefinito è sempre **null**.



| Convenzione testuale | Tipo Variant CIM | Qualificatore CIM                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **\_BSTR VT**     | **\_ convenzione testuale**: DateAndTime<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: DateAndTime<br/> **CimType**: stringa<br/>       |
| DisplayString      | **\_BSTR VT**     | **\_ convenzione testuale**: DisplayString<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: DisplayString<br/> **CimType**: stringa<br/>   |
| MacAddress         | **\_BSTR VT**     | **\_ convenzione testuale**: MacAddress<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: MacAddress<br/> **CimType**: stringa<br/>         |
| PhysAddress        | **\_BSTR VT**     | **\_ convenzione testuale**: PhysAddress<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: PhysAddress<br/> **CimType**: stringa<br/>       |
| SnmpUDPAddress     | **\_BSTR VT**     | **\_ convenzione testuale**: SnmpUDPAddress<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: SnmpUDPAddress<br/> **CimType**: stringa<br/> |
| SnmpOSIAddress     | **\_BSTR VT**     | **\_ convenzione testuale**: SnmpOSIAddress<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: SnmpOSIAddress<br/> **CimType**: stringa<br/> |
| SnmpIPXAddress     | **\_BSTR VT**     | **\_ convenzione testuale**: SnmpIPXAddress<br/> **codifica**: OCTETSTRING<br/> **\_ sintassi dell'oggetto**: SnmpIPXAddress<br/> **CimType**: stringa<br/> |



 

-   Il tipo Variant definito da CIM e i qualificatori di proprietà **CIM \_ ,** la **codifica**, **la \_ sintassi dell'oggetto** e la mappa **CimType** usando il tipo primitivo sottostante.
-   La clausola DISPLAY-HINT della macro della convenzione testuale SNMPv2C esegue il mapping Verbatim all' **\_ hint di visualizzazione** del qualificatore della proprietà CIM. Questo qualificatore non viene generato se non è presente una macro della convenzione testuale o la macro non contiene una clausola DISPLAY-HINT.

## <a name="example-code"></a>Codice di esempio

Nell'esempio seguente viene descritta una convenzione testuale SNMPv1.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

Questo esempio genera i qualificatori CIM seguenti.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

Nell'esempio seguente viene descritta una convenzione testuale SNMPv2.

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

Questo esempio genera i qualificatori CIM seguenti.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




