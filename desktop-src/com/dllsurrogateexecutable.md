---
title: DllSurrogateExecutable
description: Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del Registro di sistema DllSurrogate. Se DllSurrogateExecutable non viene specificato, COM passa NULL come valore per il primo parametro della funzione CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- DllSurrogateExecutable - valore del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fc12af22d1f85c2d2e5ff6e75b2904c5fc5eea636a64e314f997ff36a44e38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373381"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del Registro di sistema [**DllSurrogate.**](dllsurrogate.md) Se **DllSurrogateExecutable** non viene specificato, COM passa **NULL** come valore per il primo parametro della [**funzione CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Commenti

Questo valore è di tipo **REG \_ SZ**. Funziona in combinazione con il [**valore DllSurrogate**](dllsurrogate.md) per evitare ambiguità quando si usa la [**funzione CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) **DllSurrogate** indica se è necessario usare un surrogato personalizzato e queste informazioni vengono passate come primo parametro per **CreateProcess.** A seconda dell'implementazione **di CreateProcess,** queste informazioni potrebbero essere ambigue. Se **si specifica DllSurrogateExecutable,** COM passa il valore come primo parametro di **CreateProcess.** Se **DllSurrogateExecutable** non è specificato, COM passa **NULL** come valore per il primo parametro di **CreateProcess.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 