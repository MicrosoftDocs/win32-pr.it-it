---
title: /D (opzione)
description: L'opzione/D definisce un nome e un valore facoltativo da passare al preprocessore C come se fosse una direttiva \ define. In una riga di comando è possibile usare più direttive/D.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D opzione MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117088"
---
# <a name="d-switch"></a>/D (opzione)

L'opzione **/d** definisce un nome e un valore facoltativo da passare al preprocessore C come se fosse una direttiva **\# define** . In una riga di comando è possibile usare più direttive **/d** .

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*nome* 
</dt> <dd>

Specifica un nome definito che viene passato al preprocessore C quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l'opzione [**/cpp \_ opt**](-cpp-opt.md) non è presente.

</dd> <dt>

*definizione* 
</dt> <dd>

Specifica un valore associato al nome definito.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli spazi vuoti tra l'opzione **/d** e il nome definito sono facoltativi.

Quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l' [**opzione \_ /cpp opz**](-cpp-opt.md) non è, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd di/cpp** con le opzioni [**/i**](-i.md), **/d** e [**/U**](-u.md) e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF.

L'opzione del compilatore MIDL **/d** viene ignorata quando si specifica l'opzione del compilatore MIDL [/No \_ cpp](-no-cpp-nocpp.md) o [**/cpp \_ opz**](-cpp-opt.md) .

## <a name="examples"></a>Esempio

**MIDL-DUNICODE nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**\_cpp/No**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U**](-u.md)
</dt> </dl>

 

 




