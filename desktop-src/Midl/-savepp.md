---
title: Opzione /savePP
description: Quando viene specificata la direttiva /savePP, il compilatore MIDL non elimina l'output del preprocessore C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- Opzione /savePP MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c574d1032d9e392973478bc1df1e22cde6a49145b6f4775d928aac0b35e6988b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067481"
---
# <a name="savepp-switch"></a>Opzione /savePP

Quando viene **specificata la direttiva /savePP,** il compilatore MIDL non elimina l'output del preprocessore C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Questa opzione consente agli sviluppatori di distinguere ciò che viene analizzato dal compilatore MIDL ed è utile per il debug. L'output del preprocessore viene scritto in uno o più file temporanei nella directory indicata dalla variabile di ambiente TEMP. Il nome del file di output o dei file segue una convenzione di denominazione MID \* .tmp. Si noti che una singola compilazione può generare diversi flussi di input pre-elaborati. ciò è dovuto al fatto che l'importazione di un file IDL, anziché l'uso di **\# include**, causa un'esecuzione separata del preprocessore.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[/no \_ cpp, /nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




