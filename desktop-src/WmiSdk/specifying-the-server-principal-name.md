---
description: Il servizio di autenticazione Kerberos specifica il nome dell'entità server per garantire l'identità del computer a cui si connette.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Specifica del nome dell'entità server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131003"
---
# <a name="specifying-the-server-principal-name"></a>Specifica del nome dell'entità server

Il servizio di autenticazione Kerberos specifica il nome dell'entità server per garantire l'identità del computer a cui si connette. Specificare il nome dell'entità server nella chiamata al metodo di scripting [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) assegnando il nome del computer remoto. In C++ specificare il nome dell'entità server nel parametro *pServerPrincName* quando si chiama [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) per il proxy. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

Questo parametro è obbligatorio per Kerberos per supportare l'autenticazione reciproca. Tuttavia, l'utilizzo del nome dell'entità server predefinito non consente l'autenticazione reciproca. I client per i quali l'autenticazione reciproca è critica, è necessario specificare un nome di entità server corrispondente all'identità del server utilizzata dal servizio WMI. Per ulteriori informazioni sull'impostazione della sicurezza del proxy e un esempio di C++ che Mostra come impostare il nome dell'entità server, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

Per ulteriori informazioni sull'impostazione del nome dell'entità server in script e Visual Basic, vedere [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) e [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

Diversamente dalla maggior parte dei protocolli di sicurezza per Strumentazione gestione Windows (WMI) e Component Object Model (COM), non è possibile impostare l'entità server in una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Tuttavia, è possibile impostare l'entità server con il parametro *bstrAuthority* per [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)o il parametro *pServerPrincName* per [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Per eseguire correttamente la compilazione, l'esempio di codice in questo argomento richiede la seguente \# istruzione include.


```C++
#include <wbemidl.h>
```



Nell'esempio di codice seguente viene illustrato come impostare il nome dell'entità server con [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


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

[Impostazione dell'autenticazione mediante C++](setting-authentication-using-c-.md)
</dt> <dt>

[Impostazione della sicurezza in IWbemServices e in altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
