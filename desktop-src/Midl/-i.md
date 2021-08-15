---
title: Opzione /I
description: L'opzione /I specifica le directory in cui cercare i file IDL importati, i file di intestazione inclusi e i file ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- Opzione /I MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fa167ea2ef95074d201ff460eb8eece79e43442a35985921c97455f086b46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992338"
---
# <a name="i-switch"></a>Opzione /I

**L'opzione /I** specifica le directory in cui cercare i file IDL importati, i file di intestazione inclusi e i file ACF.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*percorso \_ di inclusione* 
</dt> <dd>

Specifica una o più directory che contengono file di importazione, inclusione e ACF. Lo spazio vuoto tra **l'opzione /I** e *il percorso di \_ inclusione* è facoltativo. Separare più directory con un punto e virgola (;).

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile visualizzare più directory con ogni **opzione /I** e più di un'opzione **/I** può essere visualizzata con ogni chiamata del compilatore MIDL. Le directory vengono ricercate nell'ordine in cui vengono specificate.

**L'impostazione dell'opzione /I** viene passata anche dal compilatore MIDL al preprocessore C del compilatore C. Quando l'opzione [**/cpp \_ cmd**](-cpp-cmd.md) è presente e l'opzione [**/cpp \_ opt**](-cpp-opt.md) non lo è, il compilatore MIDL concatena la stringa specificata dall'opzione **cmd \_ /cpp** con le opzioni **/I**, [**/D**](-d.md)e [**/U**](-u.md) e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF. L'opzione **/I** del compilatore MIDL non viene passata al preprocessore quando viene specificata l'opzione del compilatore MIDL **/no \_ cpp** o **/cpp \_ opt.**

Negli ambienti del sistema operativo Microsoft (Windows a 64 bit, Windows a 32 bit, Windows a 16 bit e MS-DOS), le directory vengono cercate nella sequenza seguente:

1.  La directory corrente
2.  Directory specificate **dall'opzione /I** (nell'ordine in cui seguono l'opzione )
3.  Directory specificate dalla variabile di ambiente INCLUDE

Quando le directory vengono specificate con l'opzione **/I,** l'opzione [**/no \_ def \_ idir**](-no-def-idir.md) indica al compilatore MIDL di ignorare la directory corrente, ignorare le directory specificate dalla variabile di ambiente INCLUDE ed eseguire la ricerca solo nelle directory specificate.

Quando non viene specificata alcuna directory con l'opzione **/I,** l'opzione [**/no \_ def \_ idir**](-no-def-idir.md) indica al compilatore MIDL di cercare solo la directory corrente.

## <a name="examples"></a>Esempio

**midl /I c: \\ include;c: \\ include \\ h /I \\ include2 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




