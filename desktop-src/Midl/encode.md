---
title: codifica attributo
description: L'attributo \ Encode \ ACF specifica che una routine o un tipo di dati necessita del supporto della serializzazione.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- codifica attributo MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956377"
---
# <a name="encode-attribute"></a>codifica attributo

L'attributo **\[ Encode \]** ACF specifica che una routine o un tipo di dati necessita del supporto della serializzazione.

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Specifica altri attributi che si applicano all'interfaccia nel suo complesso.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*interfaccia-definizione* 
</dt> <dd>

Specifica le istruzioni IDL che formano la definizione dell'interfaccia.

</dd> <dt>

*op-Attribute-List* 
</dt> <dd>

Specifica altri attributi operativi che si applicano alla procedura, ad esempio **\[** [**Decode**](decode.md) **\]** .

</dd> <dt>

*proc-name* 
</dt> <dd>

Specifica il nome della stored procedure.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica altri attributi applicabili al tipo, ad esempio **\[** [**Decode**](decode.md) **\]** e **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*Nome-tipo* 
</dt> <dd>

Specifica un tipo definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Encode \]** induce il compilatore MIDL a generare codice che un'applicazione può usare per serializzare i dati in un buffer. L' **\[** [](decode.md) **\]** attributo Decode genera il codice per l'unmarshalling dei dati da un buffer.

Utilizzare gli attributi **\[ Encode \]** e **\[** [**Decode**](decode.md) **\]** in un oggetto ACF per generare il codice di serializzazione per le procedure o i tipi definiti nel file IDL di un'interfaccia. Quando viene utilizzato come attributo di interfaccia, la **\[ codifica \]** viene applicata a tutti i tipi e le procedure definiti nel file IDL. Quando viene usato come attributo operativo, la **\[ codifica \]** viene applicata solo alla procedura specificata. Quando viene usato come attributo di tipo, **\[ Encode \]** si applica solo al tipo specificato.

Quando si applica l'attributo **\[ Encode \]** o **\[** [**Decode**](decode.md) **\]** a una routine, il compilatore MIDL genera uno stub di serializzazione in modo simile, perché vengono generati stub remoti per routine remote. Una routine può essere una procedura remota o di serializzazione, ma non può essere entrambe. Il prototipo della routine generata viene inviato allo STUB. File H quando lo stub entra nel \_ file c. c dello stub.

Il compilatore MIDL genera due funzioni per ogni tipo a cui viene applicato l'attributo **\[ \] Encode** e una funzione aggiuntiva per ogni tipo **\[** [](decode.md) **\]** a cui viene applicato l'attributo Decode. Ad esempio, per un tipo definito dall'utente denominato MyType, il compilatore genera il codice per le \_ funzioni MyType Encode, MyType \_ Decode e MyType \_ AlignSize. Per queste funzioni, il compilatore scrive i prototipi nello STUB. H e codice sorgente per STUB \_ C.C.

Per ulteriori informazioni sugli handle di serializzazione e sulla codifica o la decodifica dei dati, vedere [servizi di serializzazione](/windows/desktop/Rpc/serialization-services).

## <a name="examples"></a>Esempi

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocare**](allocate.md)
</dt> <dt>

[**decodificare**](decode.md)
</dt> </dl>

 

 