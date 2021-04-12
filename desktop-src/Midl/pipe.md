---
title: pipe (attributo)
description: Il costruttore del tipo di pipe consente di trasmettere un flusso aperto di dati tipizzati in una chiamata di procedura remota.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- attributo pipe MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336975"
---
# <a name="pipe-attribute"></a>pipe (attributo)

Il costruttore del tipo di **pipe** consente di trasmettere un flusso aperto di dati tipizzati in una chiamata di procedura remota.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo di elemento* 
</dt> <dd>

Definisce la dimensione di un singolo elemento nel buffer di trasferimento. Il *tipo di elemento* può essere un [tipo di base](midl-base-types.md), un \_ tipo predefinito, uno [**struct**](struct.md), un' [**enumerazione 32B**](v1-enum.md)o un identificatore di tipo. Diverse restrizioni si applicano ai *\_ tipi di elemento*, come descritto nella sezione Osservazioni riportata di seguito.

</dd> <dt>

*pipe-dichiaratore* 
</dt> <dd>

Specifica uno o più identificatori o puntatori agli identificatori. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare il costruttore del tipo di **pipe** per trasmettere i dati in entrambe le direzioni. Un **\[** [](in.md) **\]** parametro in pipe consente al server di eseguire il pull del flusso di dati dal client durante una chiamata di procedura remota. Un **\[** parametro [**out**](out-idl.md) **\]** pipe consente al server di eseguire il push del flusso di dati al client. Le routine lato client vengono fornite per eseguire il push e il pull del flusso di dati e per allocare un buffer globale per i dati. Le routine stub client e server eseguono il marshalling e l'unmarshalling dei dati e passano di nuovo un riferimento al buffer all'applicazione.

Alle pipe si applicano le restrizioni seguenti:

-   Un elemento pipe non può essere o contenere un puntatore, una matrice conforme o variabile, un handle o un handle di contesto. Inoltre, nell'implementazione Microsoft delle pipe, un elemento pipe non può essere o contenere un' [**Unione**](union.md), un' [**enumerazione 16B**](enum.md)o un [**\_ \_ int3264**](--int3264.md).
-   Non è possibile applicare gli **\[** attributi [**trasmissione \_ As**](transmit-as.md) **\]** , **\[** [**rappresenta \_ come**](represent-as.md) **\]** , **\[** [**\_ marshalling**](wire-marshal.md) **\]** o **\[** [**\_ marshalling utente**](user-marshal.md) **\]** a un tipo di pipe o al *tipo di elemento*.
-   Un tipo di pipe non può essere un membro di una struttura o di un'Unione, la destinazione di un puntatore o il tipo di base di una matrice.
-   Un tipo di dati dichiarato come un tipo di pipe può essere utilizzato solo come parametro di una chiamata remota.
-   È possibile passare un parametro pipe in entrambe le direzioni per valore o per riferimento ( **\[** puntatore [**ref**](ref.md) **\]** ). Tuttavia, non è possibile applicare l' **\[** [](ptr.md) **\]** attributo ptr a una pipe passata per riferimento. Non è possibile specificare un parametro pipe con un **\[** [](unique.md) **\]** puntatore univoco o completo, indipendentemente dalla direzione.
-   Non è possibile utilizzare pipe nelle interfacce di **\[** [**oggetti**](object.md) **\]** .
-   Non è possibile applicare l' **\[** [](idempotent.md) **\]** attributo idempotente a una routine con un parametro pipe.
-   Non è possibile usare gli attributi di serializzazione, **\[** [**codificare**](encode.md) **\]** e **\[** [**decodificare**](decode.md) **\]** con pipe.
-   Non è possibile usare handle automatici, per impostazione predefinita o con l' **\[** [**attributo \_ handle automatico**](auto-handle.md) **\]** , con pipe.

> [!Note]  
> Il compilatore MIDL supporta solo le pipe in modalità [**/OIF**](-oi.md) .

 

Per ulteriori informazioni sull'implementazione di routine con i parametri pipe, vedere [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer ' s Guide and Reference.

## <a name="examples"></a>Esempi

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**decodificare**](decode.md)
</dt> <dt>

[**codificare**](encode.md)
</dt> <dt>

[**enum**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**rappresenta \_ come**](represent-as.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**Trasmetti \_ come**](transmit-as.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[**\_marshalling utente**](user-marshal.md)
</dt> <dt>

[**\_marshalling di rete**](wire-marshal.md)
</dt> </dl>

 

 