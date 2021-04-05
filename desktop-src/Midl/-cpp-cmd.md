---
title: /cpp_cmd opzione
description: L' \_ opzione cmd/cpp specifica il preprocessore usato dal compilatore MIDL per la pre-elaborazione dei file di input.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd switch MIDL
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718697"
---
# <a name="cpp_cmd-switch"></a>\_opzione cmd/cpp

L' **opzione \_ cmd/cpp** specifica il preprocessore usato dal compilatore MIDL per la pre-elaborazione dei file di input.

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Binario per il \_ preprocessore C \_* 
</dt> <dd>

Specifica il comando che richiama il preprocessore. Questo comando consente agli sviluppatori di eseguire l'override del preprocessore predefinito. Per impostazione predefinita, MIDL richiama il compilatore Microsoft C/C++ dall'ambiente di compilazione del computer di compilazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L' *argomento \_ \_ binario del preprocessore C* per l'opzione può specificare il percorso completo. il suffisso e le virgolette di exe sono facoltativi. In genere, gli sviluppatori usano l'opzione per scegliere una particolare versione del preprocessore di Microsoft C/C++ o equivalente nell'ambiente di compilazione. In questo caso, non è necessario usare l'opzione [**/cpp \_ opt**](-cpp-opt.md) con **/cpp \_ cmd**.

Quando si usa un preprocessore non Microsoft, in particolare quando il preprocessore specificato non indirizza l'output a stdout, l'opzione del compilatore C che reindirizza l'output in stdout come parte dell'opzione [**\_ opt**](-cpp-opt.md) del compilatore MIDL/cpp deve essere specificata. Per informazioni dettagliate, vedere i [requisiti del preprocessore C per MIDL](c-preprocessor-requirements-for-midl.md)

Il preprocessore viene richiamato da una stringa di comando costituita dalle informazioni fornite al compilatore MIDL dalle opzioni **/cpp \_ cmd**, [**/cpp \_ opt**](-cpp-opt.md), [**/d**](-d.md), [**/i**](-i.md)e [**/u**](-u.md) . La tabella seguente riepiloga il modo in cui viene costruita la stringa di comando per ogni combinazione di opzioni **/cpp \_ cmd** e **/cpp \_ opz** .

Quando non si specifica l'opzione **\_ cmd/cpp** , il compilatore MIDL richiama il compilatore Microsoft C/C++. MIDL usa un file binario Cl.exe trovato nell'ambiente di compilazione.

Quando l' [**opzione \_ /cpp opt**](-cpp-opt.md) non è presente, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd/cpp** con le informazioni specificate dalle opzioni MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) . La stringa/E viene inoltre concatenata alla stringa di chiamata del compilatore C per indicare che il compilatore C/C++ deve eseguire solo la pre-elaborazione. L'opzione [**/nologo**](-nologo.md) viene aggiunta per disattivare il banner del compilatore C/C++. Il compilatore MIDL usa la stringa concatenata per richiamare il preprocessore C per l'IDL di primo livello, nonché i file IDL importati e anche per eventuali file ACF corrispondenti.

Quando è presente l'opzione [**/cpp \_ opt**](-cpp-opt.md) , che dovrebbe essere un caso raro per le piattaforme a 32 bit e a 64 bit correnti, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd/cpp** con la stringa specificata dall'opzione **/cpp \_ opt** . Il compilatore MIDL usa la stringa concatenata per richiamare il binario del preprocessore indicato al posto del preprocessore predefinito. Quando è presente l'opzione **\_ opt/cpp** , né le opzioni del compilatore MIDL specificate dalle opzioni [**/I**](-i.md), [**/d**](-d.md)e [**/u**](-u.md) né l'opzione del compilatore C/e sono concatenate alla stringa. È necessario fornire l'opzione/E, o equivalente, come parte della stringa.



| /cpp \_ cmd è presente? | /cpp \_ opt presente? | Descrizione                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| No (impostazione predefinita)       | No (impostazione predefinita)       | Richiama il compilatore Microsoft C/C++ predefinito con le impostazioni ottenute dalle opzioni MIDL [**/i**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) . Aggiunge le opzioni del preprocessore/E e [**/nologo**](-nologo.md). |
| Sì                | No                 | Richiama il file binario del preprocessore indicato con le stesse opzioni precedenti.                                                                                                                                        |
| No                 | Sì                | Richiama il compilatore Microsoft C con le opzioni specificate. Non usa le opzioni MIDL [**/i**](-i.md), [**/d**](-d.md), [**/u**](-u.md) . È necessario specificare/E come parte di [**/cpp \_ opt**](-cpp-opt.md).             |
| Sì                | Sì                | Richiama il file binario del preprocessore specificato solo con le opzioni specificate. È necessario utilizzare le virgolette.                                                                                                                       |



 

## <a name="examples"></a>Esempio

**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc nomefile. idl**

**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc nomefile. idl**

**MIDL/cpp \_ opz "/E/DFLAG = true/IC: \\ Inc" nomefile. idl**

**MIDL/cpp \_ cmd "CL"/cpp \_ opz "/e/DFLAG = true/IC: \\ Inc" nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**\_cpp/No**](-no-cpp-nocpp.md)
</dt> <dt>

[C-requisiti per il preprocessore MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




