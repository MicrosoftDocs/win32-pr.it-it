---
title: Attributo pipe
description: Il costruttore del tipo di pipe consente di trasmettere un flusso aperto di dati tipiati in una chiamata di procedura remota.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- Attributo pipe MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c407bef0a9e610d21e7221eb9a06560f33300f4f1f388fa699ca9dfb18531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641954"
---
# <a name="pipe-attribute"></a>Attributo pipe

Il **costruttore** del tipo di pipe consente di trasmettere un flusso aperto di dati tipiati in una chiamata di procedura remota.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*element-type* 
</dt> <dd>

Definisce le dimensioni di un singolo elemento nel buffer di trasferimento. *Element-type* può essere un tipo [di base,](midl-base-types.md)un tipo \_ predefinito, [**uno struct,**](struct.md) [**un'enumerazione 32b**](v1-enum.md)o un identificatore di tipo. Diverse restrizioni si applicano ai *tipi \_ di elemento*, come descritto in Note di seguito.

</dd> <dt>

*pipe-declarator* 
</dt> <dd>

Specifica uno o più identificatori o puntatori agli identificatori. Separare più dichiaratori con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile usare il costruttore **del tipo di pipe** per trasmettere dati in entrambe le direzioni. Un parametro della pipe in consente al server di eseguire il pull del flusso di **\[** [](in.md) **\]** dati dal client durante una chiamata di procedura remota. Un **\[** [**parametro out**](out-idl.md) **\]** pipe consente al server di eseguire il push del flusso di dati al client. Specificare le routine lato client per eseguire il push e il pull del flusso di dati e allocare un buffer globale per i dati. Le routine stub client e server effettuano il marshalling e l'unmarshal dei dati e passano un riferimento al buffer all'applicazione.

Alle pipe si applicano le restrizioni seguenti:

-   Un elemento pipe non può essere o contenere un puntatore, una matrice conforme o variabile, un handle o un handle di contesto. Inoltre, nell'implementazione Microsoft di pipe, un elemento pipe non può essere o contenere un'unione [**,**](union.md)un'enumerazione di [**16b**](enum.md)o [**\_ \_ un int3264**](--int3264.md).
-   Non è possibile applicare **\[** [**gli attributi transmit \_ as**](transmit-as.md) **\]** , represent **\[** [**\_ as**](represent-as.md) **\]** , wire **\[** [**\_ marshal**](wire-marshal.md)o **\]** user **\[** [**\_ marshal**](user-marshal.md) a **\]** un tipo pipe o al tipo di elemento .
-   Un tipo pipe non può essere un membro di una struttura o di un'unione, la destinazione di un puntatore o il tipo di base di una matrice.
-   Un tipo di dati dichiarato come tipo pipe può essere usato solo come parametro di una chiamata remota.
-   È possibile passare un parametro pipe in una direzione per valore o per riferimento **\[** [**(puntatore ref).**](ref.md) **\]** Non è tuttavia possibile applicare **\[** [**l'attributo ptr**](ptr.md) **\]** a una pipe passata per riferimento. Non è possibile specificare un parametro pipe con un **\[** [**puntatore univoco**](unique.md) **\]** o completo, indipendentemente dalla direzione.
-   Non è possibile usare pipe nelle **\[** [**interfacce**](object.md) **\]** a oggetti.
-   Non è possibile applicare **\[** [**l'attributo idempotente**](idempotent.md) **\]** a una routine con un parametro pipe.
-   Non è possibile usare gli attributi di **\[** [**serializzazione,**](encode.md) **\]** **\[** [**codificare e decodificare**](decode.md) **\]** con pipe.
-   Non è possibile usare handle automatici, per impostazione predefinita o con **\[** [**l'attributo di \_ gestione**](auto-handle.md) **\]** automatica, con pipe.

> [!Note]  
> Il compilatore MIDL supporta solo le pipe in [**modalità /Oif.**](-oi.md)

 

Per altre informazioni sull'implementazione di routine con parametri pipe, vedere [Pipe nella](/windows/desktop/Rpc/pipes) Guida e informazioni di riferimento per programmatori RPC.

## <a name="examples"></a>Esempi

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**handle \_ automatico**](auto-handle.md)
</dt> <dt>

[Tipi di base MIDL](midl-base-types.md)
</dt> <dt>

[**Decodificare**](decode.md)
</dt> <dt>

[**Codificare**](encode.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**Pollici**](in.md)
</dt> <dt>

[**Oggetto**](object.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**rappresentano \_ come**](represent-as.md)
</dt> <dt>

[**Struct**](struct.md)
</dt> <dt>

[**trasmettere \_ come**](transmit-as.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> <dt>

[**marshalling \_ utente**](user-marshal.md)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> </dl>

 

 