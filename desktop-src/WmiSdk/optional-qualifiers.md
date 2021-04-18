---
description: I qualificatori facoltativi indirizzano situazioni ricorrenti non comuni a tutte le implementazioni conformi a CIM, che non sono necessarie per interpretare questi qualificatori.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Qualificatori facoltativi
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318181"
---
# <a name="optional-qualifiers"></a>Qualificatori facoltativi

I qualificatori facoltativi indirizzano situazioni ricorrenti non comuni a tutte le implementazioni conformi a CIM, che non sono necessarie per interpretare questi qualificatori. I qualificatori facoltativi sono forniti nella specifica per evitare qualificatori definiti dall'utente casuali che possono verificarsi in queste situazioni ricorrenti.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Eliminare**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: associazioni, riferimenti

Per le associazioni, indica se l'associazione qualificata deve essere eliminata se uno degli oggetti a cui viene fatto riferimento nell'associazione viene eliminato e se il rispettivo oggetto a cui viene fatto riferimento nell'associazione viene qualificato con **IfDeleted**. Il valore predefinito è **false**.

Per i riferimenti, questo qualificatore indica se l'oggetto a cui si fa riferimento deve essere eliminato se l'associazione contenente il riferimento viene eliminata e qualificata con **IfDeleted** oppure se uno degli oggetti a cui viene fatto riferimento nell'associazione viene eliminato e il rispettivo oggetto a cui viene fatto riferimento nell'associazione viene qualificato con **IfDeleted**.

Utilizzo: le applicazioni devono tenere traccia delle associazioni e dei riferimenti contrassegnati con il qualificatore **Delete** ed eliminare l'associazione o il riferimento in modo appropriato. Se un oggetto nell'associazione è stato eliminato ma non è contrassegnato con **IfDeleted**, l'associazione non deve essere eliminata.

Questa regola di utilizzo deve essere verificata quando viene definito il modello di sicurezza CIM.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Costoso**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: proprietà, riferimenti, classi, associazioni, metodi

Indica se l'azione implicita richiede un calcolo esteso. Il valore predefinito è **false**.

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: associazioni e riferimenti

Indica se è necessario eliminare tutti gli oggetti all'interno di un'associazione qualificata da **Delete** se l'oggetto a cui si fa riferimento o l'associazione viene eliminato. Il valore predefinito è **false**.

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indicizzata**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: proprietà, metodi

Indica se una proprietà della classe deve essere indicizzata. Quando viene applicato alle proprietà nelle classi ospitate dal repository, questo ha il significato di creare (al momento della creazione della classe) una ricerca di query secondaria veloce per la proprietà.

È consentito solo il valore **true** (impostazione predefinita).

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisibile**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: associazioni, proprietà, metodi, riferimenti, classi

Indica se l'associazione viene definita solo per scopi interni (ad esempio, per la definizione della semantica delle dipendenze) e non deve essere visualizzata, ad esempio in maps. Il valore predefinito è **false**.

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Grandi dimensioni**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: proprietà, classi

Indica se la proprietà o la classe richiede una grande quantità di spazio di archiviazione. Il valore predefinito è **false**.

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not \_ null**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: Proprietà

Indica se una proprietà di classe non può assumere un valore **null** (**VT \_ null**). È consentito solo il valore **true** (impostazione predefinita).

Se questo qualificatore viene specificato, WMI non consente la creazione di istanze con la proprietà impostata su **null**, mentre le proprietà **null** restituiscono il codice di errore di **WBEM \_ E \_ \_ null non valido** .

Si noti che la [**chiave**](standard-qualifiers.md) e i qualificatori **indicizzati** implicano già questo comportamento.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**
</dt> <dd>

Tipo di dati: **String**

Si applica a: any

Indica che l'elemento dello schema è dinamico e quindi popolato da un provider. Il valore predefinito è **null**. Questo qualificatore è un handle specifico dell'implementazione per la strumentazione.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Sperimentale**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: any

Indica che l'elemento specificato è stato proposto come parte di una versione futura degli schemi CIM, ma non fa ancora parte dello schema standard. L'elemento è invece disponibile per consentire agli utenti di sperimentare, implementare e fornire commenti e suggerimenti su. In base ai commenti e suggerimenti, l'elemento può essere aggiunto allo standard come presentato, modificato o rimosso. Il valore predefinito è **false**. Non è necessario che un'implementazione supporti un elemento con questo qualificatore.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, riferimenti, metodi, parametri

Tipo specifico assegnato a un elemento di dati. Il valore predefinito è **null**.

Utilizzo: è necessario usare il qualificatore **SyntaxType** con questo qualificatore.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, riferimenti, metodi, parametri

Formato del qualificatore di **sintassi** . Il valore predefinito è **null**.

Utilizzo: è necessario usare il qualificatore della **sintassi** con questo qualificatore.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi, proprietà, metodi, associazioni, indicazioni, riferimenti

Circostanze in cui viene attivato un trigger. Il valore predefinito è **null**. I tipi di trigger variano in base al costrutto di Metamodello.

Per le classi e le associazioni, i valori validi sono:

Create

Delete

Aggiornamento

Access

Per le proprietà e i riferimenti, i valori validi sono: Update e Access.

Per i metodi, i valori validi sono before e After.

Per le indicazioni, viene generato il valore valido.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: Proprietà

Set di valori che indica che il valore della proprietà associata è sconosciuto (la proprietà non può essere considerata come avente un valore valido o significativo). Il valore predefinito è **null**.

Le convenzioni e le restrizioni usate per la definizione di valori sconosciuti sono le stesse applicabili al qualificatore [**ValueMap**](standard-qualifiers.md) .

Si noti che non è possibile eseguire l'override di questo qualificatore. Non è ragionevole consentire a una sottoclasse di trattare un valore come valore noto quando viene considerato sconosciuto da una classe padre.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: Proprietà

Set di valori che indica che il valore della proprietà associata non è supportato (la proprietà non può essere considerata come avente un valore valido o significativo). Il valore predefinito è **null**.

Le convenzioni e le restrizioni usate per la definizione di valori non supportati sono le stesse applicabili al qualificatore [**ValueMap**](standard-qualifiers.md) .

Nota non è possibile eseguire l'override di questo qualificatore. Non è ragionevole consentire a una sottoclasse di trattare un valore come valore supportato considerato sconosciuto da una classe padre.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Qualificatori WMI](wmi-qualifiers.md)
</dt> <dt>

[Aggiunta di un qualificatore](adding-a-qualifier.md)
</dt> </dl>

 

 




