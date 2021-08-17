---
title: notify_flag attributo
description: L'attributo \ notify \_ flag\ fornisce una notifica che identifica se viene chiamata una routine del server.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag attributo MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9fb7479667fb9757924dcba765c34138cf01c1ad6645ce7bfdc525be393e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066873"
---
# <a name="notify_flag-attribute"></a>Attributo \_ del flag notify

**\[ L'attributo del \_ flag \]** di notifica fornisce una notifica che identifica se viene chiamata una routine del server.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*procedure-name* 
</dt> <dd>

Nome della procedura remota a cui è associata la \_ procedura del flag di notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo del \_ flag \]** di notifica è simile nell'utilizzo all'attributo **\[ \] notify.**

Il **\[ nome della stored \_ procedure \]** del flag di notifica è il nome della procedura remota suffissa dal **\_ flag di \_ notifica**. La **\_ procedura del \_ flag** di notifica non richiede parametri e non restituisce un risultato. Nel file di intestazione viene generato anche un prototipo di questa procedura. Ad esempio, se il file IDL contiene quanto segue:

``` syntax
MyProcedure([in] short S);
```

Specificare quanto segue in ACF per MIDL per generare la **\_ chiamata del \_ flag di** notifica:

``` syntax
[notify_flag] MyProcedure();
```

Il compilatore MIDL genererà codice stub del server che contiene la chiamata seguente alla **\_ procedura del \_ flag di** notifica:

``` syntax
MyProcedure_notify_flag();
```

Il file di intestazione conterrà un prototipo:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ NotifyFlag** è **TRUE se** viene chiamata la routine del server.

## <a name="examples"></a>Esempi

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Notificare**](notify.md)
</dt> </dl>

 

 




