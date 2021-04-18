---
title: /sal_local opzione
description: Il \_ commutire locale/Sal indica a MIDL di generare anche le annotazioni SAL per i parametri dei metodi di interfaccia contrassegnati come \ Local \. È necessario che sia presente anche l'opzione/Sal.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local switch MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299092"
---
# <a name="sal_local-switch"></a>\_switch locale/SAL

Il commutire **\_ locale/Sal** indica a MIDL di generare anche le annotazioni SAL per i parametri dei metodi di interfaccia contrassegnati come [**\[ \] local**](local.md). È necessario che sia presente anche l'opzione [**/Sal**](-sal.md) .

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Modifica il comportamento dell'opzione [**/Sal**](-sal.md) in modo da fornire anche le annotazioni sui parametri dei metodi di interfaccia contrassegnati con l'attributo [**\[ Local \]**](local.md) . Usare l'attributo [**\[ annota \]**](annotate.md)per eseguire l'override dell'annotazione generata da MIDL con una stringa di annotazione diversa.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**\[Annotare\]**](annotate.md)
</dt> </dl>

 

 




