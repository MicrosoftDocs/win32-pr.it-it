---
title: Union (attributo)
description: La parola chiave Union viene visualizzata in funzioni correlate alle unioni discriminate.
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- attributo di Unione MIDL
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516300"
---
# <a name="union-attribute"></a>Union (attributo)

La parola chiave **Union** viene visualizzata in funzioni correlate alle unioni discriminate.

``` syntax
/* Encapsulated union*/
typedef [[ [type-attribute-list] ]] union [[ struct-name ]] switch (switch-type switch-name) [[ union-name ]] 
{
  C-style-case-list 
  [[ [ field-attribute-list <> ] ]] type-specifier <> declarator-list <>;

        ...
}

/* Non-encapsulated union*/
typedef [switch_type(switch-type) [[ , type-attr-list ]] ] union [[ tag ]] 
{ 
    [ case ( limited-expr-list) ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  [[ [ default ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  ]]
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi applicabili al tipo di Unione. Gli attributi di tipo validi includono **\[** [**handle**](handle.md) **\]** , **\[** [**trasmette \_ come**](transmit-as.md), **\]** l'attributo Pointer **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; e l' **\[** [**\_ handle di contesto**](context-handle.md) degli attributi **\]** di utilizzo e **\[** [**ignorano**](ignore.md) **\]** . Le unioni incapsulate possono anche avere l' **\[** attributo [**ref**](ref.md) **\]** pointer type. Separare più attributi con virgole.

</dd> <dt>

*struct-nome* 
</dt> <dd>

Specifica un tag facoltativo che denomina la struttura generata dal compilatore MIDL.

</dd> <dt>

*switch-type* 
</dt> <dd>

Specifica un tipo [**int**](int.md), [**char**](char-idl.md), [**enum**](enum.md) o un identificatore che viene risolto in uno di questi tipi.

</dd> <dt>

*Switch-name* 
</dt> <dd>

Specifica il nome della variabile di tipo *switch-type* che funge da discriminante di Unione.

</dd> <dt>

*nome-Unione* 
</dt> <dd>

Specifica un identificatore facoltativo che denomina l'Unione nella struttura, generata dal compilatore MIDL, che contiene l'Unione e l'discriminante.

</dd> <dt>

*Elenco di casi di tipo C* 
</dt> <dd>

Elenco di "**case** *const-expr* :"

</dd> <dt>

*elenco di espressioni limitate* 
</dt> <dd>

Specifica una o più espressioni del linguaggio C. Il compilatore MIDL supporta le espressioni condizionali, le espressioni logiche, le espressioni relazionali e le espressioni aritmetiche. MIDL non consente chiamate di funzione nelle espressioni e non consente operatori di incremento e decremento. Le singole espressioni nell'elenco devono essere separate da una virgola.

</dd> <dt>

*Field-Attribute-List* 
</dt> <dd>

Specifica zero o più attributi di campo che si applicano al membro di Unione. Gli attributi di campo validi includono **\[** [**First \_ è**](first-is.md) **\]** , **\[** [**Last \_ è**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** ; The usage Attributes **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** e **\[** [**Context \_ handle**](context-handle.md), **\]** l'attributo Pointer **\[** [**univoco**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; e, per i membri che sono unioni non incapsulate, il **\[** [**\_ tipo di opzione**](switch-type.md)dell'attributo Union **\]** . Le unioni non incapsulate possono anche usare l' **\[** [](ref.md) **\]** attributo del campo Ref Pointer. Separare più attributi di campo con virgole.

</dd> <dt>

*identificatore di tipo* 
</dt> <dd>

Specifica un [tipo di base](midl-base-types.md), uno [**struct**](struct.md), un' **Unione**, un tipo [**enum**](enum.md) o un identificatore di tipo. Una specifica di archiviazione facoltativa può precedere *Type-specifier*.

</dd> <dt>

*elenco di dichiaratori* 
</dt> <dd>

Uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici. I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle unioni trasmesse in chiamate a procedure remote. Tranne quando si usa l'opzione del compilatore MIDL [**/OSF**](-osf.md), questi dichiaratori sono consentiti nelle unioni non trasmesse. Separare più dichiaratori con virgole.

</dd> <dt>

*tag* 
</dt> <dd>

Specifica un tag facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

MIDL supporta due tipi di unioni discriminate, ovvero [unioni](encapsulated-unions.md) incapsulate e unioni non [incapsulate](nonencapsulated-unions.md). L'Unione incapsulata è compatibile con le implementazioni precedenti di RPC (garante della versione 1). L'Unione non incapsulata Elimina alcune restrizioni dell'Unione incapsulata e fornisce un discriminante più visibile rispetto all'Unione incapsulata.

L'Unione incapsulata è identificata dalla parola chiave [**Switch**](switch.md) e dall'assenza di altre parole chiave correlate all'Unione.

L'Unione non incapsulata, nota anche come Unione, è identificata dalla presenza dell' **\[** [**opzione \_**](switch-is.md) **\]** e dalle **\[** parole chiave di [**\_ tipo switch**](switch-type.md) **\]** , che identificano discriminante e il relativo tipo.

Quando si utilizza **\[** [**in**](in.md), [](out-idl.md) le **\]** unioni out, tenere presente che la modifica del valore dell'opzione Union durante la chiamata può rendere il comportamento della chiamata remota in modo diverso da una chiamata locale. Al ritorno, gli stub copiano il parametro **\[ in**, **out \]** in memoria che è già presente nel client. Quando la procedura remota modifica il valore dell'opzione Union e, di conseguenza, modifica la dimensione dell'oggetto dati, gli stub possono sovrascrivere la memoria valida con il valore **\[ out \]** . Quando l'opzione di Unione modifica l'oggetto dati da un tipo di base a un tipo di puntatore, gli stub possono sovrascrivere la memoria valida quando copiano il referente del puntatore nella posizione di memoria indicata dall'oggetto **\[ in \]** valore di un tipo di base.

La forma delle unioni deve essere identica tra le diverse piattaforme per garantire l'interconnettività.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Unioni incapsulate](encapsulated-unions.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[Unioni non incapsulate](nonencapsulated-unions.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**opzione \_**](switch-is.md)
</dt> <dt>

[**tipo di opzione \_**](switch-type.md)
</dt> </dl>

 

 




