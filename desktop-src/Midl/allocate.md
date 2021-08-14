---
title: allocare l'attributo
description: L'attributo \ allocate\ ACF consente di personalizzare l'allocazione e la deallocazione della memoria per un tipo definito nel file IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- allocare l'attributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345652b9da5ed5087793606d963d6cf9b8ce225587ee150c27f6410ae99b8d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808443"
---
# <a name="allocate-attribute"></a>allocare l'attributo

**\[ L'attributo allocate \]** ACF consente di personalizzare l'allocazione e la deallocazione della memoria per un tipo definito nel file IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*allocate-option-list* 
</dt> <dd>

Specifica una o più opzioni di allocazione della memoria. Selezionare uno dei **nodi \_ singoli** o di  tutti i nodi oppure uno dei due, gratuito o non gratuito, oppure uno da ogni coppia. **\_** **\_** Quando si specificano più opzioni, separare le opzioni con virgole.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica altri attributi facoltativi di tipo ACF. Quando si specificano più attributi di tipo, separare le opzioni con virgole.

</dd> <dt>

*type-name* 
</dt> <dd>

Specifica un tipo definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo allocate \]** ha le opzioni valide seguenti.



| Opzione           | Descrizione                                                           |
|------------------|-----------------------------------------------------------------------|
| **tutti i \_ nodi**   | Esegue una chiamata per allocare e liberare memoria per tutti i nodi.             |
| **nodo \_ singolo** | Esegue molte chiamate singole per allocare e liberare ogni nodo di memoria. |
| **free**         | Libera memoria al ritorno dallo stub del server.                          |
| **don't \_ free**   | Non libera memoria al ritorno dallo stub del server.                  |



 

Per impostazione predefinita, gli stub possono allocare spazio di archiviazione per i dati a cui fa riferimento un puntatore univoco o completo chiamando [**midl \_ user \_ allocate**](midl-user-allocate-1.md) e [**midl \_ user \_ free**](midl-user-free-1.md) singolarmente per ogni puntatore.

È possibile ottimizzare la velocità dell'applicazione specificando l'opzione tutti **i \_ nodi**. Questa opzione indica allo stub di calcolare le dimensioni di tutta la memoria a cui si fa riferimento tramite il puntatore del tipo specificato ed eseguire una singola chiamata all'allocazione [**\_ dell'utente \_ midl.**](midl-user-allocate-1.md) Lo stub rilascia la memoria effettuando una chiamata a [**midl \_ user \_ free**](midl-user-free-1.md).

**L'opzione don't \_ free** indica al compilatore MIDL di generare uno stub del server che non chiama [**l'utente midl \_ \_ free**](midl-user-free-1.md) per il tipo specificato. **L'opzione don't \_ free** consente alle strutture del puntatore di rimanere accessibili all'applicazione server dopo che la chiamata di procedura remota è stata completata e restituita al client.

**\[ L'attributo allocate \]** farà sì che qualsiasi parametro **\[ in, out \]** che sia un puntatore a un tipo qualificato con l'opzione **tutti \_** i nodi rialloci la memoria quando i dati vengono disassociati. È responsabilità dell'applicazione liberare la memoria allocata in precedenza per questo parametro. Esempio:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

Il tipo di dati PTHISTYPE verrà riallocato nella direzione [**\[ di \]**](out-idl.md) uscita dallo stub prima di eseguire l'unmarsshaling. Pertanto, l'applicazione deve liberare la memoria allocata in precedenza per i dati di questo parametro, in caso contrario si verificherà una perdita di memoria.

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

[**Pollici**](in.md)
</dt> <dt>

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




