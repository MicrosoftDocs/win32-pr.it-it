---
title: Opzione /U
description: L'opzione /U rimuove qualsiasi definizione precedente di un nome passando il nome al preprocessore C come se fosse una direttiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- Opzione /U MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895771"
---
# <a name="u-switch"></a>Opzione /U

**L'opzione /U** rimuove qualsiasi definizione precedente di un nome passando il nome al preprocessore C come se fosse una **\# direttiva undefine.**

``` syntax
midl /U name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*nome* 
</dt> <dd>

Specifica un nome definito da passare al preprocessore C come se fosse una **\# direttiva undefine.** Il nome è predefinito dal preprocessore C o definito in precedenza dall'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

In **una riga di** comando è possibile usare più direttive /U. Lo spazio vuoto tra **l'opzione /U** e il nome non definito è facoltativo.

Quando l'opzione [**/cpp \_ cmd**](-cpp-cmd.md) è presente e l'opzione [**/cpp \_ opt**](-cpp-opt.md) non lo è, il compilatore MIDL concatena la stringa specificata dall'opzione /cpp cmd con le opzioni \_ [**/I**](-i.md), [**/D**](-d.md)e **/U** e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF. L'opzione **/U** del compilatore MIDL viene ignorata quando viene specificata l'opzione del compilatore MIDL **/no \_ cpp** o **/cpp \_ opt.**

## <a name="examples"></a>Esempio

**midl /UUNICODE filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/d**](-d.md)
</dt> <dt>

[**/i**](-i.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




