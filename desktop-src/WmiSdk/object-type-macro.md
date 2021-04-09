---
description: La macro di tipo oggetto contiene clausole obbligatorie e facoltative che descrivono le caratteristiche di base di un oggetto MIB. Il provider SNMP converte un MIB nelle parti corrispondenti della macro del tipo di oggetto.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro di tipo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128078"
---
# <a name="object-type-macro"></a>Macro di tipo oggetto

La macro di tipo oggetto contiene clausole obbligatorie e facoltative che descrivono le caratteristiche di base di un oggetto MIB. Il provider SNMP converte un MIB nelle parti corrispondenti della macro del tipo di oggetto.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Componenti

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Oggetto MIB
</dt> <dd>

Oggetto che contiene la maggior parte dei dati in questione.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descrittore di oggetto
</dt> <dd>

Nome univoco o descrittore di oggetto che identifica ogni oggetto MIB. Ogni descrittore di oggetti MIB viene mappato esattamente a un nome di proprietà CIM. Ad esempio, **ifindex** viene convertito in **ifindex**.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Clausola SYNTAX](syntax-clause.md)
</dt> <dd>

Definisce i dati e il tipo di un oggetto MIB.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Clausola INDEX](index-clause.md)
</dt> <dd>

Definisce una chiave per la selezione di una riga di tabella univoca.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Clausola AUGMENTs
</dt> <dd>

Indica che la raccolta di tabelle specificata può essere considerata un'estensione di un'altra raccolta di tabelle e può sostituire la clausola INDEX in SNMPv2. Le raccolte a cui fa riferimento la clausola AUGMENTs possono essere combinate con l'altra raccolta di tabelle per formare una raccolta. La raccolta risultante condivide le proprietà della chiave primaria specificate nell'ultima raccolta di tabelle nella catena.

In questo caso, le regole di mapping precedenti specificate per la clausola INDEX vengono applicate all'ultima raccolta di tabelle nella catena. La raccolta di oggetti viene quindi mappata a una definizione di classe CIM.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Clausola dell'identificatore di oggetto
</dt> <dd>

Contiene un identificatore di oggetto univoco per un oggetto MIB. Questo identificatore di oggetto esegue il mapping all' **\_ identificatore di oggetto** qualificatore della proprietà CIM.

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Clausole ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)
</dt> <dd>

Definire i diritti di accesso all'oggetto MIB.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Clausola DESCRIPTION
</dt> <dd>

Fornisce una descrizione di testo dell'oggetto, che esegue il mapping alla **Descrizione** del qualificatore della proprietà CIM. Questa clausola può essere vuota.

Ogni oggetto **Table** e **entry** in una definizione di tabella SNMP contiene anche una clausola Description, che può anche essere vuota. Le clausole della descrizione della tabella e della voce sono concatenate e il risultato viene mappato alla **Descrizione** del qualificatore della classe CIM.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clausola STATUS
</dt> <dd>

Indica se l'oggetto deve essere supportato. Quando il valore della clausola STATUS è **obsoleto**, il provider elimina l'oggetto MIB dal mapping. In caso contrario, la clausola STATUS viene mappata allo **stato** del qualificatore della proprietà CIM.

Per SNMPv1, il valore preferito dello **stato** è **obbligatorio** o **facoltativo**, ma il qualificatore può contenere un altro valore. Per SNMPv2C, il valore preferito dello **stato** è **Current** o **deprecato**, ma il qualificatore può contenere un altro valore.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Clausola DEFVAL
</dt> <dd>

Assegna un valore predefinito a una variabile in una riga della tabella logica ed esegue il mapping al qualificatore di proprietà CIM della stringa **DEFVAL**.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Clausola REFERENCE
</dt> <dd>

Fa riferimento a un altro documento che contiene ulteriori informazioni sull'oggetto. Questa clausola esegue il mapping al **riferimento** al qualificatore di proprietà CIM, che è di tipo String.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Clausola UNITs
</dt> <dd>

Fornisce una definizione precisa degli elementi rappresentati dall'oggetto. Questa clausola esegue il mapping alle **unità** del qualificatore di proprietà CIM, che è di tipo String.

</dd> </dl>

## <a name="remarks"></a>Commenti

La macro di tipo oggetto descrive le caratteristiche di base di un singolo oggetto MIB. Un set di macro di tipo oggetto può essere considerato un gruppo di oggetti correlati. In SNMPv2C utilizzare la macro del gruppo di oggetti per raggruppare in modo formale i set di oggetti correlati in una raccolta. Tuttavia, non esiste un meccanismo formale per la creazione di raccolte in SNMPv1. Ai fini del provider SNMP, la macro del gruppo di oggetti viene ignorata, ma è possibile inventare relazioni di raggruppamento e creare raccolte di infrastruttura.

 

 



