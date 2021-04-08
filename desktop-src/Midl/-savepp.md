---
title: opzione/savePP
description: Quando si specifica la direttiva/savePP, il compilatore MIDL non elimina l'output del preprocessore C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP switch MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045759"
---
# <a name="savepp-switch"></a>opzione/savePP

Quando si specifica la direttiva **/savePP** , il compilatore MIDL non elimina l'output del preprocessore C/C++.

``` syntax
midl /savePP
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Questa opzione consente agli sviluppatori di discernere gli elementi analizzati dal compilatore MIDL ed è utile per il debug. L'output del preprocessore viene scritto in uno o più file temporanei nella directory indicata dalla variabile di ambiente TEMP. Il nome del file di output, o file, segue una convenzione di denominazione di MID \* . tmp. Si noti che una singola compilazione può generare diversi flussi di input pre-elaborati. Ciò è dovuto al fatto che l'importazione di un file IDL, anziché l'utilizzo di **\# include**, comporta l'esecuzione di un preprocessore separato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[/No \_ cpp,/nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




