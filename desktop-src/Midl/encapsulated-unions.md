---
title: Unioni incapsulate
description: Un'Unione contenuta con il relativo discriminante in una struttura all'interno di è un'Unione incapsulata.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- tipi di dati MIDL, unioni incapsulate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298837"
---
# <a name="encapsulated-unions"></a>Unioni incapsulate

Un'Unione contenuta con il relativo discriminante in una struttura all'interno di è un'Unione incapsulata. L'Unione incapsulata è indicata dalla presenza della parola chiave [**Switch**](switch.md) . Questo tipo di Unione è così denominato perché il compilatore MIDL incapsula automaticamente l'Unione e il relativo discriminante in una struttura per la trasmissione durante una chiamata di procedura remota.

Se manca il tag Union (tipo U1 \_ nell'esempio precedente), il compilatore genererà la struttura con il campo Union denominato *Tagged \_ Union*.

La forma delle unioni deve essere identica tra le varie piattaforme per garantire l'interconnettività.

Per una descrizione del formato di un'Unione incapsulata, vedere [**Union**](union.md).

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

Per informazioni correlate, vedere [tipi di base MIDL](midl-base-types.md), [**char**](char-idl.md), **\[** [**\_ handle di contesto**](context-handle.md) **\]** , [**enum**](enum.md), **\[** [**First \_ is**](first-is.md) **\]** , **\[** [**handle**](handle.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** , [**int**](int.md), **\[** [**Ignore**](ignore.md) **\]** , **\[** [**Last \_ is**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [unincapsulated Unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** , **\[** [**String**](string.md) **\]** , [**struct**](struct.md), [**Switch**](switch.md), Switch **\[** [**\_ is**](switch-is.md) **\]** , **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**trasmissione \_ As**](transmit-as.md) **\]** , [**Union**](union.md)e **\[** [**Unique**](unique.md)**\]**

 

 




