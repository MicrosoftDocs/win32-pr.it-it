---
title: Opzione /D
description: L'opzione /D definisce un nome e un valore facoltativo da passare al preprocessore C come se fosse una direttiva \ define. In una riga di comando è possibile usare più direttive /D.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- Opzione /D MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8bc01a978949ec0f0cc4ff78289a1cb442046966f1cea954c6b65cc232f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385778"
---
# <a name="d-switch"></a>Opzione /D

**L'opzione /D** definisce un nome e un valore facoltativo da passare al preprocessore C come se fosse una **\# direttiva define.** In **una riga di** comando è possibile usare più direttive /D.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*nome* 
</dt> <dd>

Specifica un nome definito che viene passato al preprocessore C quando è presente l'opzione [**\_ cmd /cpp**](-cpp-cmd.md) e l'opzione [**/cpp \_ opt**](-cpp-opt.md) non è presente.

</dd> <dt>

*Definizione* 
</dt> <dd>

Specifica un valore associato al nome definito.

</dd> </dl>

## <a name="remarks"></a>Commenti

Lo spazio vuoto tra **l'opzione /D** e il nome definito è facoltativo.

Quando l'opzione [**cmd \_ /cpp**](-cpp-cmd.md) è presente e l'opzione [**/cpp \_ opt**](-cpp-opt.md) non lo è, il compilatore MIDL concatena la stringa specificata dall'opzione **/cpp \_ cmd** con le opzioni [**/I**](-i.md), **/D** e [**/U**](-u.md) e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF.

L'opzione **/D** del compilatore MIDL viene ignorata quando viene specificata l'opzione del compilatore MIDL [/no \_ cpp](-no-cpp-nocpp.md) o [**/cpp \_ opt.**](-cpp-opt.md)

## <a name="examples"></a>Esempio

**midl -DUNICODE filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/i**](-i.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**/u**](-u.md)
</dt> </dl>

 

 




