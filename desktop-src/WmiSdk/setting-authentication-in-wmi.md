---
description: Quando si effettuano chiamate all'esterno del processo chiamante o a un servizio WMI remoto, WMI utilizza la versione distribuita del Component Object Model (DCOM).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Impostazione dell'autenticazione in WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232394"
---
# <a name="setting-authentication-in-wmi"></a>Impostazione dell'autenticazione in WMI

Quando si effettuano chiamate all'esterno del processo chiamante o a un servizio WMI remoto, WMI utilizza la versione distribuita del Component Object Model (DCOM). Le chiamate out-of-process e remote vengono eseguite tramite proxy, che richiedono l'autenticazione delle credenziali del processo chiamante.

È possibile impostare il livello di autenticazione quando ci si connette a un computer e a uno spazio dei nomi WMI. Per connettersi a WMI, chiamare [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) in C++. Per la creazione di script o Visual Basic, connettersi a WMI utilizzando SWbemLocator. ConnectServer o tramite la stringa del [moniker](constructing-a-moniker-string.md) . Per la sicurezza DCOM e WMI sono necessari determinati livelli di autenticazione quando ci si connette tra computer. Il livello richiesto varia in base al sistema operativo che si sta connettendo. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

WMI viene in genere eseguito in un host del servizio condiviso e condivide la stessa autenticazione di altri processi nell'host. Per eseguire il processo WMI con un livello di autenticazione diverso, eseguire WMI con il comando [**WinMgmt**](winmgmt.md) con l'opzione **/standalonehost** e impostare il livello di autenticazione per WMI in genere. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

Per ulteriori informazioni ed esempi di codice su come impostare l'autenticazione per le connessioni WMI, vedere [impostazione del servizio di autenticazione tramite VBScript](setting-the-authentication-service-using-vbscript.md) e [impostazione dell'autenticazione mediante C++](setting-authentication-using-c-.md). Questi argomenti contengono anche le tabelle in cui sono elencate le costanti di autenticazione per C++ e lo scripting.

## <a name="using-proxies-in-wmi"></a>Utilizzo di proxy in WMI

Per impostare l'autenticazione per un proxy, chiamare la funzione [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Per ulteriori informazioni e un esempio di codice, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

L' [API com seguente per](com-api-for-wmi.md) gli oggetti WMI usa i proxy direttamente in C++ o C# per chiamare out-of-process o a un servizio WMI remoto:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Gli oggetti di scripting, ad esempio [**SWbemObject**](swbemobject.md), [**SWbemServices**](swbemservices.md)e [**SWbemRefresher**](swbemrefresher.md) , non utilizzano direttamente proxy. Gli oggetti di scripting rappresentano invece un wrapper o un livello che effettua chiamate nell' [API com per](com-api-for-wmi.md) gli oggetti WMI elencati in precedenza. Per ulteriori informazioni e un esempio di codice relativo all'impostazione dell'autenticazione nello scripting, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
