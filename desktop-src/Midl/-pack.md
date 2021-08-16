---
title: Opzione /pack
description: L'opzione /pack corrisponde all'opzione /Zp .
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- Opzione /pack MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9282cd5ab56d2e037ba585676a83c5cd558ecb26354ab191899ad341506f5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991943"
---
# <a name="pack-switch"></a>Opzione /pack

**L'opzione /pack** corrisponde [**all'opzione /Zp**](-zp.md) .

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*livello di \_ packing* 
</dt> <dd>

Specifica il livello di creazione di un pacchetto di strutture nel sistema di destinazione. Il valore del livello di packing può essere impostato su 1, 2, 4 o 8.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'opzione /pack** definisce il livello di creazione di un pacchetto di strutture nel sistema di destinazione. Il valore del livello di pacchetto corrisponde al [**valore dell'opzione /Zp**](-zp.md) usato dal compilatore Microsoft C/C++ versione 7.0. Per altre informazioni, vedere la documentazione sulla programmazione microsoft C/C++.

Specificare lo stesso livello di creazione di pacchetto quando si richiama il compilatore MIDL e il compilatore C. Il livello di packing predefinito usato quando l'opzione [**/Zp**](-zp.md) o **/pack** non è specificata è 8, in entrambi gli ambienti di compilazione.

Per una descrizione dei potenziali rischi per l'uso di livelli di packing non standard, vedere l'argomento della Guida [**/Zp.**](-zp.md)

## <a name="examples"></a>Esempio

**midl /pack 2 filename.idl**

**midl /pack 8 bar.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




