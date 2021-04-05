---
title: Switch/u
description: L'opzione/U rimuove tutte le definizioni precedenti di un nome passando il nome al preprocessore C come se fosse una direttiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U switch MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117041"
---
# <a name="u-switch"></a>Switch/u

L'opzione **/u** rimuove tutte le definizioni precedenti di un nome passando il nome al preprocessore C come se fosse una direttiva **\# undefine** .

``` syntax
midl /U name
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*nome* 
</dt> <dd>

Specifica un nome definito da passare al preprocessore C come se fosse una direttiva **\# undefine** . Il nome è predefinito dal preprocessore C o definito in precedenza dall'utente.

</dd> </dl>

## <a name="remarks"></a>Commenti

In una riga di comando è possibile usare più direttive **/u** . Gli spazi vuoti tra l'opzione **/u** e il nome non definito sono facoltativi.

Quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l'opzione [**/cpp \_ opz**](-cpp-opt.md) non è, il compilatore MIDL concatena la stringa specificata dall' \_ opzione cmd di/cpp con le opzioni [**/i**](-i.md), [**/d**](-d.md)e **/u** e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF. L'opzione **/u** del compilatore MIDL viene ignorata quando si specifica l'opzione del compilatore MIDL **/No \_ cpp** o **/cpp \_ opz** .

## <a name="examples"></a>Esempio

**MIDL/UUNICODE nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**\_cpp/No**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




