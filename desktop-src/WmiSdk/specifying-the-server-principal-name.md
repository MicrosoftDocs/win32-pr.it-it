---
description: Il servizio di autenticazione Kerberos specifica il nome dell'entità server per garantire l'identità del computer a cui si connette.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Specifica del nome dell'entità server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b3d05d6933653a7d2a1737d36f00f6ca65c39bd7739e5f2e9f4232eb507f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816424"
---
# <a name="specifying-the-server-principal-name"></a>Specifica del nome dell'entità server

Il servizio di autenticazione Kerberos specifica il nome dell'entità server per garantire l'identità del computer a cui si connette. Specificare il nome dell'entità server nella chiamata al metodo di scripting [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) specificando il nome del computer remoto. In C++ specificare il nome dell'entità server nel parametro *pServerPrincName* quando si chiama [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per il proxy. Per altre informazioni, vedere [Connessione a WMI in un computer remoto.](connecting-to-wmi-on-a-remote-computer.md)

Questo parametro è obbligatorio per il supporto dell'autenticazione reciproca da parte di Kerberos. Tuttavia, l'utilizzo del nome dell'entità server predefinita non consente l'autenticazione reciproca. I client per cui l'autenticazione reciproca è critica devono specificare un nome dell'entità server corrispondente all'identità del server utilizzato dal servizio WMI. Per altre informazioni sull'impostazione della sicurezza del proxy e un esempio di C++ che illustra come impostare il nome dell'entità server, vedere Impostazione della sicurezza in [IWbemServices](setting-the-security-on-iwbemservices-and-other-proxies.md)e altri proxy.

Per altre informazioni sull'impostazione del nome dell'entità server nello script e Visual Basic, vedere [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) e Connessione a WMI in [un computer remoto.](connecting-to-wmi-on-a-remote-computer.md)

A differenza della maggior parte dei protocolli di sicurezza per Windows Management Instrumentation (WMI) e Component Object Model (COM), non è possibile impostare l'entità server in una chiamata a [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) È tuttavia possibile impostare l'entità server con il parametro *bstrAuthority* per [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)o il parametro *pServerPrincName* per [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

L'esempio di codice in questo argomento richiede la corretta \# compilazione dell'istruzione include seguente.


```C++
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come impostare il nome dell'entità server [**con ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione del servizio di autenticazione tramite VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Impostazione dell'autenticazione tramite C++](setting-authentication-using-c-.md)
</dt> <dt>

[Impostazione della sicurezza in IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
