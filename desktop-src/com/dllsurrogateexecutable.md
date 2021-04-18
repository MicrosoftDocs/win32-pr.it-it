---
title: DllSurrogateExecutable
description: Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del registro di sistema DllSurrogate. Se DllSurrogateExecutable viene omesso, COM passa NULL come valore per il primo parametro della funzione CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valore DllSurrogateExecutable del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300555"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del registro di sistema [**DllSurrogate**](dllsurrogate.md) . Se **DllSurrogateExecutable** viene omesso, com passa **null** come valore per il primo parametro della funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Commenti

Questo valore è di tipo **reg \_ SZ**. Funziona insieme al valore [**DllSurrogate**](dllsurrogate.md) per evitare ambiguità quando si usa la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . **DllSurrogate** indica se è necessario usare un surrogato personalizzato e queste informazioni vengono passate come primo parametro per **CreateProcess**. A seconda dell'implementazione di **CreateProcess**, le informazioni potrebbero essere ambigue. Se viene specificato **DllSurrogateExecutable** , com passa il valore come primo parametro di **CreateProcess**. Se **DllSurrogateExecutable** viene omesso, com passa **null** come valore per il primo parametro di **CreateProcess**.

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

 

 