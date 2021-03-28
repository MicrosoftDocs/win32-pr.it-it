---
description: È possibile testare i valori del flag SFGAO degli attributi della Shell per un elemento per determinare se il verbo deve essere abilitato o disabilitato.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Come usare gli attributi degli elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881557"
---
# <a name="how-to-use-item-attributes"></a>Come usare gli attributi degli elementi

È possibile testare i valori del flag [**SFGAO**](sfgao.md) degli attributi della Shell per un elemento per determinare se il verbo deve essere abilitato o disabilitato.

Per usare questa funzionalità di attributo, aggiungere i seguenti valori **reg \_ DWORD** sotto il verbo:

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Il valore AttributeMask specifica il valore [**SFGAO**](sfgao.md) dei valori di bit della maschera con cui eseguire il test.

### <a name="step-2"></a>Passaggio 2:

Il valore AttributeValue specifica il valore [**SFGAO**](sfgao.md) dei bit sottoposti a test.

### <a name="step-3"></a>Passaggio 3:

ImpliedSelectionModel specifica zero per i verbi di elemento o un valore diverso da zero per i verbi nel menu di scelta rapida in background.

## <a name="remarks"></a>Commenti

Nell'esempio seguente di voce del registro di sistema, AttributeMask è impostato su [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

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

 

 



