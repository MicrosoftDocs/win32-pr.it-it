---
title: opzione/Pack
description: L'opzione/Pack è uguale all'opzione/Zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /Pack switch MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045860"
---
# <a name="pack-switch"></a>opzione/Pack

L'opzione **/Pack** è uguale all'opzione [**/ZP**](-zp.md) .

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*livello di compressione \_* 
</dt> <dd>

Specifica il livello di compressione delle strutture nel sistema di destinazione. Il valore a livello di compressione può essere impostato su 1, 2, 4 o 8.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione **/Pack** designa il livello di compressione delle strutture nel sistema di destinazione. Il valore a livello di compressione corrisponde al valore dell'opzione [**/ZP**](-zp.md) usato dal compilatore Microsoft C/C++ versione 7,0. Per ulteriori informazioni, vedere la documentazione sulla programmazione in Microsoft C/C++.

Specificare lo stesso livello di compressione quando si richiama il compilatore MIDL e il compilatore C. Il livello di compressione predefinito utilizzato quando non viene specificata né l'opzione [**/ZP**](-zp.md) né **/Pack** è 8, in entrambi gli ambienti di compilazione.

Per una descrizione dei potenziali rischi correlati all'uso di livelli di compressione non standard, vedere l'argomento della Guida di [**/ZP**](-zp.md) .

## <a name="examples"></a>Esempio

**MIDL/Pack 2 nomefile. idl**

**MIDL/Pack 8 bar. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ENV**](-env.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




