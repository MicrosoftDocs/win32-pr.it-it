---
title: midl_pragma attributo di avviso
description: Usare l' \_ opzione MIDL pragma warning per eseguire temporaneamente l'override del comportamento del messaggio di avviso di MIDL in fase di compilazione.
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- attributo MIDL di avviso midl_pragma
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857225"
---
# <a name="midl_pragma-warning-attribute"></a>\_attributo pragma warning di MIDL

Usare l'opzione **MIDL \_ pragma warning** per eseguire temporaneamente l'override del comportamento del messaggio di avviso di MIDL in fase di compilazione.

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*\_opzione warning* 
</dt> <dd>

L'opzione di avviso può essere una delle seguenti: Disabilita, Abilita, valore predefinito.

</dd> <dt>

*\_elenco messaggi* 
</dt> <dd>

Elenco di numeri di messaggio separati da spazi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il pragma può essere usato come un pragma del compilatore C. Ovvero Disabilita, Abilita o restituisce il comportamento predefinito per un determinato avviso MIDL.

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

 

 




