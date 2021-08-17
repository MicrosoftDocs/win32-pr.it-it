---
title: midl_pragma di avviso
description: Usare l'opzione pragma warning midl per eseguire temporaneamente l'override del comportamento dei messaggi di avviso \_ midl in fase di compilazione.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma'attributo di avviso MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae8e902d1e58ff216f36ae8003dc8f3f553a32005136ef2a86201bd17279107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067091"
---
# <a name="midl_pragma-warning-attribute"></a>Attributo pragma warning midl \_

Usare **l'opzione pragma \_ warning midl** per eseguire temporaneamente l'override del comportamento dei messaggi di avviso midl in fase di compilazione.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*opzione \_ warning* 
</dt> <dd>

L'opzione warning può essere una delle seguenti: disable, enable, default.

</dd> <dt>

*elenco \_ di messaggi* 
</dt> <dd>

Elenco di numeri di messaggio separati da spazi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il pragma può essere usato come un pragma del compilatore C. Ciò significa che disabilita, abilita o torna al comportamento predefinito per un determinato avviso MIDL.

## <a name="examples"></a>Esempi

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**pragma**](pragma.md)
</dt> </dl>

 

 




