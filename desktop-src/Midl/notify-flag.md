---
title: attributo notify_flag
description: L'attributo \ Notify \_ flag \ fornisce una notifica che identifica se viene chiamata una routine del server.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- attributo notify_flag MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045566"
---
# <a name="notify_flag-attribute"></a>notifica \_ flag-attributo

L'attributo **\[ Notify \_ flag \]** fornisce una notifica che identifica se viene chiamata una routine del server.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome procedura* 
</dt> <dd>

Nome della procedura remota a cui \_ è associata la procedura relativa al flag di notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Notify \_ flag \]** è simile nell'utilizzo dell'attributo **\[ Notify \]** .

Il nome della procedura del **\[ \_ flag \] di notifica** è il nome della procedura remota con suffisso per **\_ notifica \_ flag**. La procedura di **\_ notifica del \_ flag** non richiede alcun parametro e non restituisce alcun risultato. Nel file di intestazione viene anche generato un prototipo di questa procedura. Ad esempio, se il file IDL contiene quanto segue:

``` syntax
MyProcedure([in] short S);
```

Specificare quanto segue in ACF per MIDL per generare la chiamata al **\_ \_ flag di notifica** :

``` syntax
[notify_flag] MyProcedure();
```

Il compilatore MIDL genererà il codice stub del server che contiene la chiamata seguente alla procedura relativa al **\_ \_ flag di notifica** :

``` syntax
MyProcedure_notify_flag();
```

Il file di intestazione conterrà un prototipo:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ PARETE NOTIFYFLAG** è **true** se viene chiamata la routine del server.

## <a name="examples"></a>Esempi

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**comunica**](notify.md)
</dt> </dl>

 

 




