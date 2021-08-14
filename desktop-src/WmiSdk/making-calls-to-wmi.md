---
description: I provider possono chiamare i metodi implementati da WMI dall'interno delle implementazioni dei metodi.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Esecuzione di chiamate a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76adae33db786a8174879e6c7e88b62fb69f3c59598ae7f055f41865b32dbf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317675"
---
# <a name="making-calls-to-wmi"></a>Esecuzione di chiamate a WMI

I provider possono chiamare i metodi implementati da WMI dall'interno delle implementazioni dei metodi. Esistono tuttavia considerazioni speciali quando un provider chiama l'implementazione WMI di un metodo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) dall'interno della propria implementazione dello stesso metodo. Queste considerazioni sono importanti indipendentemente dal fatto che il provider chiami la versione sincrona o asincrona del metodo .

Ogni [**metodo IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che un provider può implementare ha un *parametro pCtx,* un puntatore a un'implementazione dell'interfaccia [**IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) Quando WMI chiama il provider, WMI passa un puntatore valido in questo parametro. Un provider deve sempre passare questo stesso puntatore in tutte le chiamate a WMI effettuate durante la manutenzione delle richieste. Se non si imposta *pCtx in* modo appropriato, WMI può avviare un ciclo infinito.

L'esempio di codice seguente illustra il modo corretto per chiamare l'implementazione WMI di [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) dall'interno di un'implementazione di [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



L'esempio di codice C++ in questo argomento richiede i riferimenti seguenti e \# le istruzioni include per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



I provider di istanze, classi e proprietà non devono eseguire chiamate a WMI che richiedono la modifica dei dati durante la manutenzione di una richiesta di lettura. Gli unici provider che sono eccezioni a questa regola sono i provider push. Un provider push è un provider di classi che archivia i dati nel repository WMI e si basa su WMI per gestire le richieste dai client. Durante la manutenzione di una richiesta di lettura, un provider push può aggiornare il repository WMI, ma deve impostare il parametro *lFlags* su **WBEM \_ FLAG OWNER \_ \_ UPDATE** nella chiamata [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) appropriata.

I provider di eventi non devono apportare modifiche alla classe durante la manutenzione di una chiamata. Non possono inoltre eseguire chiamate correlate agli eventi, ad esempio la modifica di un filtro eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> </dl>

 

 



