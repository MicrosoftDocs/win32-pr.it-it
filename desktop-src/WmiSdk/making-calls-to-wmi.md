---
description: I provider possono chiamare i metodi implementati da WMI all'interno delle implementazioni del metodo.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Esecuzione di chiamate a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050061"
---
# <a name="making-calls-to-wmi"></a>Esecuzione di chiamate a WMI

I provider possono chiamare i metodi implementati da WMI all'interno delle implementazioni del metodo. Tuttavia, esistono considerazioni speciali quando un provider chiama l'implementazione WMI di un metodo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) dall'interno della propria implementazione dello stesso metodo. Queste considerazioni sono importanti a prescindere dal fatto che il provider chiami la versione sincrona o asincrona del metodo.

Ogni metodo [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che un provider può implementare ha un parametro *pctX* , un puntatore a un'implementazione dell'interfaccia [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) . Quando WMI chiama il provider, WMI passa un puntatore valido in questo parametro. Un provider deve sempre passare questo stesso puntatore in tutte le chiamate a WMI effettuate durante la manutenzione delle richieste. Se si trascura di impostare *pctX* in modo appropriato, WMI può avviare un ciclo infinito.

Nell'esempio di codice seguente viene illustrato il modo corretto per chiamare l'implementazione WMI di [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) dall'interno di un'implementazione di [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


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



Nell'esempio di codice C++ in questo argomento sono necessari i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



I provider di istanze, classi e proprietà non devono eseguire alcuna chiamata a WMI che richiede la modifica dei dati durante la manutenzione di una richiesta di lettura. Gli unici provider che sono eccezioni a questa regola sono i provider di push. Un provider di push è un provider di classi che archivia i dati nel repository WMI e si basa su WMI per gestire le richieste provenienti dai client. Durante la manutenzione di una richiesta di lettura, un provider di push può aggiornare il repository WMI, ma è necessario impostare il parametro *è* sull' **aggiornamento del \_ proprietario del flag \_ \_ WBEM** nella chiamata [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) appropriata.

I provider di eventi non devono apportare modifiche alle classi durante la manutenzione di una chiamata. Non possono anche emettere chiamate relative agli eventi, ad esempio la modifica di un filtro eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> </dl>

 

 



