---
description: La macro OBJECT-TYPE contiene clausole obbligatorie e facoltative che descrivono le caratteristiche di base di un oggetto MIB. Il provider SNMP converte un MIB nelle parti corrispondenti della macro OBJECT-TYPE.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: OBJECT-TYPE Macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef71bcdd915dfaa59ace008c28a5d63a323c2cd1d0f119b9d91e5a0720e192e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818007"
---
# <a name="object-type-macro"></a>OBJECT-TYPE Macro

La macro OBJECT-TYPE contiene clausole obbligatorie e facoltative che descrivono le caratteristiche di base di un oggetto MIB. Il provider SNMP converte un MIB nelle parti corrispondenti della macro OBJECT-TYPE.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Configurazione dell'ambiente SNMP WMI.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="components"></a>Componenti

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Oggetto MIB
</dt> <dd>

Oggetto che contiene la maggior parte dei dati in questione.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descrittore di oggetto
</dt> <dd>

Nome univoco o descrittore di oggetto che identifica ogni oggetto MIB. Ogni descrittore di oggetto MIB esegue esattamente il mapping a un nome di proprietà CIM. Ad esempio, **ifIndex** converte in **ifIndex**.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Clausola SYNTAX](syntax-clause.md)
</dt> <dd>

Definisce i dati e il tipo di un oggetto MIB.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Clausola INDEX](index-clause.md)
</dt> <dd>

Definisce una chiave per la selezione di una riga di tabella univoca.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Clausola AUGMENTS
</dt> <dd>

Indica che la raccolta di tabelle specificata può essere considerata un'estensione di un'altra raccolta di tabelle e può sostituire la clausola INDEX in SNMPv2. Le raccolte a cui fa riferimento la clausola AUGMENTS possono essere combinate con l'altra raccolta di tabelle per formare una raccolta. La raccolta risultante condivide le proprietà della chiave primaria specificate nell'ultima raccolta di tabelle nella catena.

In questo caso, le regole di mapping precedenti specificate per la clausola INDEX vengono applicate all'ultima raccolta di tabelle nella catena. La raccolta di oggetti viene quindi mappata a una definizione di classe CIM.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Clausola OBJECT-IDENTIFIER
</dt> <dd>

Contiene un identificatore di oggetto univoco per un oggetto MIB. Questo identificatore di oggetto esegue il mapping all'identificatore di oggetto del qualificatore di proprietà CIM . **\_**

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Clausole ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)
</dt> <dd>

Definire i diritti di accesso all'oggetto MIB.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Clausola DESCRIPTION
</dt> <dd>

Fornisce una descrizione testuale dell'oggetto , che esegue il mapping al qualificatore di proprietà CIM **Description**. Questa clausola può essere vuota.

Ogni **oggetto TABLE** e **ENTRY** in una definizione di tabella SNMP contiene anche una clausola DESCRIPTION, che può anche essere vuota. Le clausole TABLE e ENTRY DESCRIPTION vengono concatenate e il risultato viene mappato al qualificatore di classe CIM **Description**.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clausola STATUS
</dt> <dd>

Indica se l'oggetto deve essere supportato. Quando il valore della clausola STATUS è **obsoleto,** il provider rimuove l'oggetto MIB dal mapping. In caso contrario, la clausola STATUS viene mappata al qualificatore di proprietà CIM **Status**.

Per SNMPv1, il valore preferito  di **Status** è obbligatorio o facoltativo, ma il qualificatore può contenere un altro valore. Per SNMPv2C, il valore preferito di **Status** è **current** o **deprecato,** ma il qualificatore può contenere un altro valore.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Clausola DEFVAL
</dt> <dd>

Assegna un valore predefinito a una variabile in una riga di tabella logica ed esegue il mapping al qualificatore di proprietà CIM della stringa **Defval**.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Clausola REFERENCE
</dt> <dd>

Fa riferimento a un altro documento che contiene altre informazioni sull'oggetto . Questa clausola esegue il mapping al qualificatore di proprietà CIM **Reference**, che è di tipo string.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Clausola UNITS
</dt> <dd>

Fornisce una definizione precisa di ciò che rappresenta l'oggetto . Questa clausola esegue il mapping al qualificatore di proprietà CIM **Units**, che è di tipo string.

</dd> </dl>

## <a name="remarks"></a>Commenti

La macro OBJECT-TYPE descrive le caratteristiche di base di un singolo oggetto MIB. Un set di macro OBJECT-TYPE può essere considerato come un gruppo di oggetti correlati. In SNMPv2C usare la macro OBJECT-GROUP per raggruppare formalmente set di oggetti correlati in una raccolta. Tuttavia, non esiste alcun meccanismo formale per la creazione di raccolte in SNMPv1. Ai fini del provider SNMP, la macro OBJECT-GROUP viene ignorata, ma è possibile inventare relazioni di raggruppamento e creare raccolte.

 

 



