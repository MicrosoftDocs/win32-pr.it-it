---
description: I valori del flag SFGAO degli attributi shell per un elemento possono essere testati per determinare se il verbo deve essere abilitato o disabilitato.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Come usare gli attributi degli elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ddcc567a820ba1d9c1394ca38f78fc9ce9ec634596f8dbe41feca9def32e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859570"
---
# <a name="how-to-use-item-attributes"></a>Come usare gli attributi degli elementi

I valori del flag [**SFGAO**](sfgao.md) degli attributi shell per un elemento possono essere testati per determinare se il verbo deve essere abilitato o disabilitato.

Per usare questa funzionalità dell'attributo, aggiungere i valori **\_ DWORD REG** seguenti sotto il verbo:

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Il valore AttributeMask specifica il [**valore SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.

### <a name="step-2"></a>Passaggio 2:

Il valore AttributeValue specifica il [**valore SFGAO**](sfgao.md) dei bit che vengono testati.

### <a name="step-3"></a>Passaggio 3:

ImpliedSelectionModel specifica zero per i verbi elemento o diverso da zero per i verbi nel menu di scelta rapida in background.

## <a name="remarks"></a>Commenti

Nella voce del Registro di sistema di esempio seguente AttributeMask è impostato su [**SFGAO \_ READONLY**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



