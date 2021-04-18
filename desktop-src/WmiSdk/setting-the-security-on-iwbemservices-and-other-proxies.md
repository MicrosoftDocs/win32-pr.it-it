---
description: "In C++ è possibile impostare la sicurezza per l'intero processo chiamando CoInitializeSecurity prima di connettersi a WMI tramite IWbemLocator:: ConnectServer."
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Impostazione della sicurezza in IWbemServices e in altri proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d593c52091182b1f0580908624e0b4068ed3f8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318518"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Impostazione della sicurezza in IWbemServices e in altri proxy

In C++ è possibile impostare la sicurezza per l'intero processo chiamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) prima di connettersi a WMI tramite [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). È anche possibile modificare il livello di autenticazione, il livello di rappresentazione o il servizio di autenticazione in una chiamata che ottiene un puntatore a un proxy WMI, ad esempio [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult). La chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) consente inoltre di modificare il servizio di autenticazione (Kerberos, NTLM o Negotiate).

Gli script e le applicazioni Visual Basic consentono solo di impostare la sicurezza sui proxy indirettamente tramite chiamate a [**SWbemServices**](swbemservices.md) e ad altri oggetti di automazione. Per ulteriori informazioni sull'impostazione e la modifica dell'autenticazione e della rappresentazione nello script, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

La modifica dei livelli di sicurezza o dei servizi rappresenta principalmente un problema quando ci si connette a WMI in un computer remoto in cui è in esecuzione un sistema operativo diverso. Per ulteriori informazioni, vedere [connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Un'applicazione client si connette a un proxy WMI utilizzando un'identità. Un'identità è un oggetto dati costituito da un nome utente, una password e le impostazioni dell'autorità. Per un'applicazione client WMI, la chiamata all'interfaccia [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) crea l'identità iniziale. Il metodo [**ConnectServer**](swbemlocator-connectserver.md) acquisisce l'identità in un set di tre parametri, che è possibile impostare su **null** per indicare l'utente corrente. È anche possibile specificare un parametro non **null** per indicare un utente e un dominio specifici. Se la chiamata ha esito positivo, **ConnectServer** restituisce un puntatore tramite il quale è possibile accedere a un'ampia gamma di processi remoti, ad esempio un servizio WMI o direttamente il sistema operativo Windows.

Analogamente a molte interfacce COM, [**ConnectServer**](swbemlocator-connectserver.md) restituisce un puntatore a un proxy. Un proxy è un oggetto dati che rappresenta un processo remoto, ad esempio WMI o un provider remoto. COM utilizza un proxy per consentire agli sviluppatori di accedere ai dati remoti come se i dati fossero locali.

Le interfacce WMI seguenti usano i proxy:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (oggetto di scripting [**SWbemServices**](swbemservices.md) )
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (oggetto di scripting [**SWbemRefresher**](swbemrefresher.md) )

    L'aggiornamento di WMI è un caso speciale perché viene passato un puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , le cui impostazioni di sicurezza devono essere impostate correttamente. Per ulteriori informazioni sull'utilizzo di oggetti di aggiornamento, vedere [accesso ai dati sulle prestazioni in C++](accessing-performance-data-in-c--.md).

Dopo aver ricevuto un puntatore a un processo remoto, è possibile eseguire una delle due operazioni seguenti. Se si conosce il funzionamento del processo, è possibile scegliere di impostare la sicurezza sull'indicatore di misura e accedere normalmente al processo. Questo è il caso della maggior parte dei puntatori a un servizio WMI. Per ulteriori informazioni, vedere [impostazione dei livelli di sicurezza in una connessione WMI](setting-the-security-levels-on-a-wmi-connection.md). In alternativa, è necessario accedere a un'interfaccia COM diversa sul proxy, ad esempio [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), tramite una chiamata all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sul proxy.

## <a name="defaults-and-recommendations"></a>Impostazioni predefinite e consigli

La versione distribuita del Component Object Model (DCOM) negozia il servizio di autenticazione predefinito (Kerberos, NTLM o Negotiate) e non è possibile specificare il servizio di autenticazione predefinito utilizzando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). Specificando il **\_ \_ \_ valore predefinito auth C AuthN** nel parametro del servizio di autenticazione di [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) , DCOM potrà selezionare il servizio appropriato. Per le connessioni remote il servizio predefinito è Negotiate, ovvero il servizio consigliato per le applicazioni che funzionano nei domini Kerberos e non Kerberos. Per le connessioni locali, il servizio di autenticazione predefinito è NT LAN Manager (NTLM).

Nell'esempio di codice seguente viene illustrato il servizio di autenticazione predefinito utilizzato.


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



Per l'esempio di codice in questo argomento sono necessarie le \# istruzioni Reference e include seguenti.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Per gli script, è consigliabile usare i valori predefiniti che DCOM seleziona per le chiamate remote. Nel computer locale non è possibile specificare un servizio di autenticazione per le chiamate a WMI. Per ulteriori informazioni, vedere [impostazione del servizio di autenticazione tramite VBScript](setting-the-authentication-service-using-vbscript.md) e [creazione di una stringa del moniker](constructing-a-moniker-string.md).

 

 
