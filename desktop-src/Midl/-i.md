---
title: Opzione/i
description: L'opzione/I specifica le directory in cui ricercare i file IDL importati, i file di intestazione inclusi e i file ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I switch MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045836"
---
# <a name="i-switch"></a>Opzione/i

L'opzione **/i** specifica le directory in cui ricercare i file IDL importati, i file di intestazione inclusi e i file ACF.

``` syntax
midl /I include_path
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Includi \_ percorso* 
</dt> <dd>

Specifica una o più directory che contengono file di importazione, inclusione e ACF. Gli spazi vuoti tra l'opzione **/i** e il *\_ percorso di inclusione* sono facoltativi. Separare più directory con un carattere punto e virgola (;).

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile visualizzare più directory con ogni opzione **/i** e più di un'opzione **/i** può comparire con ogni chiamata del compilatore MIDL. Viene eseguita la ricerca nelle directory nell'ordine in cui sono specificate.

L'impostazione dell'opzione **/i** viene passata anche dal compilatore MIDL al preprocessore c del compilatore c. Quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l' [**opzione \_ /cpp opz**](-cpp-opt.md) non è, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd di/cpp** con le opzioni **/i**, [**/d**](-d.md)e [**/U**](-u.md) e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF. L'opzione del compilatore MIDL **/i** non viene passata al preprocessore quando si specifica l'opzione del compilatore MIDL **/No \_ cpp** o **/cpp \_ opz** .

Negli ambienti del sistema operativo Microsoft (Windows a 64 bit, Windows a 32 bit, Windows a 16 bit e MS-DOS), le directory vengono ricercate nella sequenza seguente:

1.  La directory corrente
2.  Directory specificate dall'opzione **/i** (nell'ordine in cui seguono l'opzione)
3.  Directory specificate dalla variabile di ambiente INCLUDE

Quando si specificano le directory con l'opzione **/i** , l'opzione [**/No \_ def \_ Idir**](-no-def-idir.md) indica al compilatore MIDL di ignorare la directory corrente, ignorare le directory specificate dalla variabile di ambiente include e cercare solo le directory specificate.

Quando non viene specificata alcuna directory con l'opzione **/i** , l'opzione [**/No \_ def \_ Idir**](-no-def-idir.md) indica al compilatore MIDL di eseguire la ricerca solo nella directory corrente.

## <a name="examples"></a>Esempio

**MIDL/I c: \\ include; c: \\ Includi \\ h/i \\ INCLUDE2 nomefile. idl**

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

[**/No \_ def \_ Idir**](-no-def-idir.md)
</dt> </dl>

 

 




