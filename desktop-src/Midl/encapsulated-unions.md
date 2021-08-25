---
title: Unioni incapsulate
description: Un'unione contenuta con la relativa discriminante in una struttura all'interno di è un'unione incapsulata.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- tipi di dati MIDL, unioni incapsulate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc8f8f830d49430551af7d6450b0174742b9436afcdba764e9fa6494c957d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895361"
---
# <a name="encapsulated-unions"></a>Unioni incapsulate

Un'unione contenuta con la relativa discriminante in una struttura all'interno di è un'unione incapsulata. L'unione incapsulata è indicata dalla presenza della parola chiave [**switch.**](switch.md) Questo tipo di unione è così denominato perché il compilatore MIDL incapsula automaticamente l'unione e la relativa discriminante in una struttura per la trasmissione durante una chiamata di procedura remota.

Se il tag union non è presente (U1 TYPE nell'esempio precedente), il compilatore genererà la struttura con il campo \_ union denominato con tag *\_ union*.

La forma delle unioni deve essere la stessa tra le piattaforme per garantire l'interconnettività.

Per una descrizione del formato di un'unione incapsulata, vedere [**union**](union.md).

## <a name="examples"></a>Esempio

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

Per informazioni correlate, vedere [MidL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[** [**context \_ handle**](context-handle.md) **\]** , [**enum**](enum.md), **\[** [**first \_ is**](first-is.md) **\]** , **\[** [**handle**](handle.md) **\]** , **\[** [**ignore**](ignore.md) **\]** , [**int**](int.md), ignore , **\[** [**last**](ignore.md) **\]** **\[** [**\_ is**](last-is.md) **\]** , length **\[** [**\_ is**](length-is.md) **\]** , max **\[** [**\_ is**](max-is.md) **\]** , ms **\[** [**\_ union**](ms-union-attrib.md) **\]** , [Nonencapsulated Unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , ref , **\[** [**size**](ref.md) **\]** **\[** [**\_ is**](size-is.md) **\]** , **\[** [**string**](string.md) **\]** , [**struct**](struct.md), [**switch**](switch.md), **\[** [**switch \_ is**](switch-is.md), switch **\]** **\[** [**\_ type**](switch-type.md) **\]** , transmit **\[** [**\_ as**](transmit-as.md) **\]** , [**union**](union.md)e **\[** [**unique**](unique.md)**\]**

 

 




