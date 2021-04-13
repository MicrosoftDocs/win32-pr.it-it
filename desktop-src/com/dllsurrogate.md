---
title: DllSurrogate
description: Consente l'esecuzione di server DLL in un processo surrogato. Se viene specificata una stringa vuota, viene utilizzato il surrogato fornito dal sistema; in caso contrario, il valore specifica il percorso del surrogato da usare.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Valore DllSurrogate del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399770"
---
# <a name="dllsurrogate"></a>DllSurrogate

Consente l'esecuzione di server DLL in un processo surrogato. Se viene specificata una stringa vuota, viene utilizzato il surrogato fornito dal sistema; in caso contrario, il valore specifica il percorso del surrogato da usare.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica che la classe è una dll che deve essere attivata in un processo surrogato e il processo surrogato da usare. Per usare il processo surrogato generico fornito dal sistema, impostare il *percorso* su una stringa vuota o su **null**. Per specificare un altro processo surrogato, impostare *path* sul percorso del surrogato. Come nella specifica del percorso di un server sotto la chiave [**LocalServer32**](localserver32.md) , non è necessario specificare un percorso completo. È necessario scrivere il surrogato per comunicare correttamente con il servizio DCOM come descritto in [scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md).

Il valore **DllSurrogate** deve essere presente affinché un server DLL venga attivato in un surrogato. L'attivazione fa riferimento a una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). L'esecuzione di dll in un processo surrogato offre i vantaggi di un'implementazione eseguibile, tra cui l'isolamento degli errori, la possibilità di gestire più client simultaneamente e consente al server di fornire servizi ai client remoti in un ambiente distribuito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Surrogati DLL](dll-surrogates.md)
</dt> <dt>

[**DllSurrogateExecutable**](dllsurrogateexecutable.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 