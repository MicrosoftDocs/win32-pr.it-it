---
title: /cpp_opt opzione
description: L' \_ opzione/cpp opz specifica le opzioni da passare al preprocessore C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt switch MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104399997"
---
# <a name="cpp_opt-switch"></a>/cpp \_ opz switch

L'opzione **/cpp \_ opz** specifica le opzioni da passare al preprocessore C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*C ( \_ opzione del preprocessore) \_* 
</dt> <dd>

Specifica l'opzione della riga di comando associata al preprocessore richiamato. 

**Nota**: per i preprocessori di Microsoft C/C++, è necessario specificare l'opzione `/E` come parte della stringa di *\_ \_ opzione del preprocessore c* . 

Le virgolette sono obbligatorie quando viene usata più di un'opzione e per gli spazi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non utilizzare questa opzione a meno che non esista un motivo specifico per questa operazione. Per informazioni importanti sulla pre-elaborazione, vedere [requisiti per il preprocessore per MIDL](c-preprocessor-requirements-for-midl.md) .

È possibile usare l'opzione **/cpp \_ opt** con o senza l' [**opzione \_ cmd di/cpp**](-cpp-cmd.md) . Per informazioni dettagliate sul modo in cui la riga di comando del preprocessore viene costruita in entrambi i casi, vedere **/cpp \_ cmd** .

L'opzione **/cpp \_ opt** , se specificata, deve sempre includere per `/E` funzionare correttamente.

## <a name="examples"></a>Esempio

**MIDL/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc nomefile. idl**

**MIDL/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc nomefile. idl**

**MIDL/cpp \_ opz "/E/DFLAG = true/IC: \\ Inc" nomefile. idl**

**MIDL/cpp \_ cmd "CL"/cpp \_ opz "/e/DFLAG = true/IC: \\ Inc" nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**\_cpp/No**](-no-cpp-nocpp.md)
</dt> <dt>

[C-requisiti per il preprocessore MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




