---
title: Opzione /no_robust
description: L'opzione /no robust indica al compilatore MIDL di disabilitare in modo esplicito la funzionalità della riga \_ di comando /robust. L'opzione della riga di comando /robust e le funzionalità associate sono l'impostazione predefinita del compilatore per MIDL versione 6.0.359 e successive.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- Opzione /no_robust MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808856"
---
# <a name="no_robust-switch"></a>/no \_ robust switch

**L'opzione /no \_ robust** indica al compilatore MIDL di disabilitare in modo esplicito la funzionalità della riga di comando [**/robust.**](-robust.md) L'opzione della riga di comando **/robust** e le funzionalità associate sono l'impostazione predefinita del compilatore per MIDL versione 6.0.359 e successive.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Con MIDL versione 6.0.359 e successive, il compilatore MIDL [**imposta /robust**](-robust.md) per impostazione predefinita. **L'opzione \_ della** riga di comando /no robust deve essere usata per disabilitare la funzionalità **/robust** se gli stub generati devono essere eseguiti in Microsoft Windows NT, Windows 95/98 o Windows Me.

## <a name="examples"></a>Esempio

**midl /no \_ robust filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




