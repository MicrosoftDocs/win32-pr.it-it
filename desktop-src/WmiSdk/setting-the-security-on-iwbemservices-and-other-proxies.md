---
description: In C++ è possibile impostare la sicurezza per l'intero processo chiamando CoInitializeSecurity prima di connettersi a WMI tramite IWbemLocator::ConnectServer.
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Impostazione della sicurezza in IWbemServices e altri proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da997b9d4a8f91cf31e8619af983209d4a07a571932c85304d372379d7f752b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050269"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Impostazione della sicurezza in IWbemServices e altri proxy

Mentre in C++ è possibile impostare la sicurezza per l'intero processo chiamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) prima di connettersi a WMI tramite [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). È anche possibile modificare il livello di autenticazione, il livello di rappresentazione o il servizio di autenticazione in una chiamata che ottiene un puntatore a un proxy WMI, ad esempio [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o [**IWbemCallResult.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) La [**chiamata a CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) consente anche di modificare il servizio di autenticazione (Kerberos, NTLM o negotiate).

Gli script Visual Basic applicazioni impostano la sicurezza sui proxy solo indirettamente tramite chiamate a [**SWbemServices**](swbemservices.md) e ad altri oggetti di automazione. Per altre informazioni sull'impostazione e sulla modifica dell'autenticazione e della rappresentazione nello script, vedere Impostazione del livello di sicurezza del processo [predefinito tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

La modifica dei livelli di sicurezza o dei servizi è principalmente un problema quando ci si connette a WMI in un computer remoto che esegue un sistema operativo diverso. Per altre informazioni, vedere [Connessione tra sistemi operativi diversi.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)

Un'applicazione client si connette a un proxy WMI usando un'identità. Un'identità è un oggetto dati costituito da un nome utente, una password e le impostazioni dell'autorità. Per un'applicazione client WMI, la chiamata [**all'interfaccia IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) crea l'identità iniziale. Il [**metodo ConnectServer**](swbemlocator-connectserver.md) accetta l'identità in un set di tre parametri, che è possibile impostare su **NULL** per indicare l'utente corrente. È anche possibile specificare un parametro non **NULL** per indicare un utente e un dominio specifici. Se la chiamata ha esito positivo, **ConnectServer** restituisce un puntatore tramite il quale è possibile accedere direttamente a un'ampia gamma di processi remoti, ad esempio un servizio WMI o il Windows operativo.

Come molte interfacce COM, [**ConnectServer**](swbemlocator-connectserver.md) restituisce un puntatore a un proxy. Un proxy è un oggetto dati che rappresenta un processo remoto, ad esempio WMI o un provider remoto. COM usa un proxy per consentire agli sviluppatori di accedere ai dati remoti come se i dati fossero locali.

Le interfacce WMI seguenti usano i proxy:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (oggetto di scripting [**SWbemServices)**](swbemservices.md)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (oggetto di scripting [**SWbemRefresher)**](swbemrefresher.md)

    L'aggiornamento WMI è un caso speciale perché viene passato un puntatore [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) le cui impostazioni di sicurezza devono essere impostate correttamente. Per altre informazioni sull'uso degli oggetti di aggiornamento, vedere [Accesso ai dati sulle prestazioni in C++.](accessing-performance-data-in-c--.md)

Dopo aver ricevuto un puntatore a un processo remoto, è possibile eseguire una delle due operazioni seguenti. Se si conosce il processo, è possibile scegliere di impostare la sicurezza sul puntatore e accedere normalmente al processo. Questo è il caso della maggior parte dei puntatori a un servizio WMI. Per altre informazioni, vedere [Impostazione dei livelli di sicurezza in una connessione WMI.](setting-the-security-levels-on-a-wmi-connection.md) In alternativa, è necessario accedere a un'interfaccia COM diversa nel proxy, ad esempio [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), tramite una chiamata [**all'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nel proxy.

## <a name="defaults-and-recommendations"></a>Impostazioni predefinite e Consigli

La versione distribuita del Component Object Model (DCOM) negozia il servizio di autenticazione predefinito (Kerberos, NTLM o Negotiate) e non è possibile specificare il servizio di autenticazione predefinito usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Se si **specifica RPC \_ C \_ AUTHN \_ DEFAULT nel** parametro del servizio di autenticazione di [**CoSetProxyBlanket,**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) DCOM può selezionare il servizio appropriato. Per le connessioni remote il servizio predefinito è Negotiate, che è il servizio consigliato per le applicazioni che funzionano sia in domini Kerberos che non Kerberos. Per le connessioni locali, il servizio di autenticazione predefinito è NT LAN Manager (NTLM).

Nell'esempio di codice seguente viene illustrato il servizio di autenticazione predefinito in uso.


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



L'esempio di codice in questo argomento richiede le istruzioni reference e \# include seguenti.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Per gli script, è consigliabile usare le impostazioni predefinite selezionate da DCOM per le chiamate remote. Nel computer locale non è possibile specificare un servizio di autenticazione per le chiamate a WMI. Per altre informazioni, vedere [Impostazione del servizio di autenticazione tramite VBScript](setting-the-authentication-service-using-vbscript.md) e Costruzione di una stringa [moniker.](constructing-a-moniker-string.md)

 

 
