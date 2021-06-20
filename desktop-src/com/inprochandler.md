---
title: InprocHandler
description: InprocHandler specifica se un'applicazione usa un gestore personalizzato nella chiave HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID del Registro di sistema.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aea1ca0d5eb5dec58a36578d268d7020a963a95e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404734"
---
# <a name="inprochandler"></a>InprocHandler

Specifica se un'applicazione usa un gestore personalizzato.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ** che specifica il gestore personalizzato usato dall'applicazione. Se non viene usato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.

Se un contenitore cerca un gestore personalizzato nel Registro di sistema, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




