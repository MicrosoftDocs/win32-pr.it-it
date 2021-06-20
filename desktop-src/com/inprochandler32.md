---
title: InprocHandler32
description: InprocHandler32 specifica se un'applicazione usa un gestore personalizzato nella chiave HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID registro di sistema.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Chiave del Registro di sistema COM InprocHandler32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73a8b2577a554b0bb8b5ba5a851e630edbf90a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406004"
---
# <a name="inprochandler32"></a>InprocHandler32

Specifica se un'applicazione usa un gestore personalizzato.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Commenti

Si tratta di **un \_ valore REG SZ** che specifica il gestore personalizzato usato dall'applicazione. Se non viene usato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.

Se un contenitore cerca nel Registro di sistema un gestore personalizzato, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




