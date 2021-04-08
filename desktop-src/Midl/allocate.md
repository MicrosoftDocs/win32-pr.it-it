---
title: alloca attributo
description: L'attributo \ allocate \ ACF consente di personalizzare l'allocazione e la deallocazione della memoria per un tipo definito nel file IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- alloca attributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857270"
---
# <a name="allocate-attribute"></a>alloca attributo

L'attributo **\[ allocate \]** ACF consente di personalizzare l'allocazione e la deallocazione della memoria per un tipo definito nel file IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*allocate-Option-List* 
</dt> <dd>

Specifica una o più opzioni di allocazione della memoria. Selezionare uno dei nodi **a \_ nodo singolo** o a **tutti i \_ nodi** oppure una delle due coppie **disponibili** o **non \_ disponibili**. Quando si specifica più di un'opzione, separare le opzioni con virgole.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica altri attributi di tipo ACF facoltativi. Quando si specifica più di un attributo di tipo, separare le opzioni con virgole.

</dd> <dt>

*Nome-tipo* 
</dt> <dd>

Specifica un tipo definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ allocate \]** presenta le seguenti opzioni valide.



| Opzione           | Descrizione                                                           |
|------------------|-----------------------------------------------------------------------|
| **tutti i \_ nodi**   | Effettua una chiamata per allocare e liberare memoria per tutti i nodi.             |
| **\_nodo singolo** | Esegue molte chiamate singole per allocare e liberare ogni nodo di memoria. |
| **free**         | Libera la memoria al ritorno dallo stub del server.                          |
| **non \_ liberare**   | Non libera la memoria al ritorno dallo stub del server.                  |



 

Per impostazione predefinita, gli stub possono allocare spazio di archiviazione per i dati a cui fa riferimento un puntatore univoco o completo chiamando l' [**\_ utente MIDL \_ allocate**](midl-user-allocate-1.md) e l' [**\_ utente MIDL \_ gratuitamente**](midl-user-free-1.md) singolarmente per ogni puntatore.

È possibile ottimizzare la velocità dell'applicazione specificando l'opzione **tutti i \_ nodi**. Questa opzione indica allo stub di calcolare la dimensione di tutta la memoria a cui viene fatto riferimento tramite il puntatore del tipo specificato e di eseguire una singola chiamata [**all' \_ utente MIDL \_ allocate**](midl-user-allocate-1.md). Lo stub rilascia la memoria rendendo disponibile una sola chiamata [**a \_ MIDL \_ User**](midl-user-free-1.md).

L'opzione Not **\_ Free** indica al compilatore MIDL di generare uno stub del server che non chiama [**\_ \_ Free User MIDL**](midl-user-free-1.md) per il tipo specificato. L'opzione Not **\_ Free** consente alle strutture del puntatore di rimanere accessibili all'applicazione server dopo che la chiamata RPC è stata completata e restituita al client.

L'attributo **\[ allocate \]** provocherà qualsiasi parametro **\[ in \] , out** che è un puntatore a un tipo qualificato con l'opzione **All \_ Nodes** per riallocare la memoria quando viene eseguito l'unmarshalling dei dati. È responsabilità dell'applicazione liberare la memoria allocata in precedenza per questo parametro. Ad esempio:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

Il tipo di dati PTHISTYPE verrà riallocato nella direzione di [**\[ uscita \]**](out-idl.md) dallo stub prima dell'unmarshalling. Pertanto, l'applicazione deve liberare la memoria allocata in precedenza per i dati di questo parametro o si verificherà una perdita di memoria.

## <a name="examples"></a>Esempi

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**\_alloca utente \_ MIDL**](midl-user-allocate-1.md)
</dt> <dt>

[**\_utente MIDL \_ gratuito**](midl-user-free-1.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




