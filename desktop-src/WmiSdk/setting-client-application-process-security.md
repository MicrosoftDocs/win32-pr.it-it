---
description: Le applicazioni client che chiamano interfacce WMI possono controllare i livelli di sicurezza dei propri processi.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Impostazione della sicurezza del processo dell'applicazione client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bfa0a42390ffa433cff01300b0976d40553665c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232393"
---
# <a name="setting-client-application-process-security"></a>Impostazione della sicurezza del processo dell'applicazione client

Le applicazioni client che chiamano interfacce WMI possono controllare i livelli di sicurezza dei propri processi. Tutte le applicazioni WMI accedono a WMI tramite COM ed è possibile chiamare la funzione COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza per i processi. Le applicazioni che effettuano chiamate asincrone a WMI e alle applicazioni che si registrano come consumer di eventi impostano livelli di sicurezza sulla chiamata in WMI.

Se non si effettua una chiamata esplicita a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), com lo chiama in modo implicito con i valori del registro di sistema. Tuttavia, i valori del registro di sistema possono avere impostazioni inferiori per la rappresentazione e l'autenticazione che non forniscono la sicurezza necessaria per WMI. Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito mediante C++](setting-the-default-process-security-level-using-c-.md).

L'accesso asincrono a WMI non è consigliato. Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione sincrona o semisincrono o eseguire controlli di accesso appropriati nell'applicazione client. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Le chiamate a qualsiasi proxy WMI ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)o [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) utilizzano un puntatore out-of-process. Per ulteriori informazioni sui valori predefiniti e sulle raccomandazioni, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

Nella procedura riportata di seguito vengono descritti i passaggi da eseguire per impostare la sicurezza per WMI nel processo dell'applicazione.

**Per impostare la sicurezza per WMI nel processo dell'applicazione**

1.  Determinare i livelli di sicurezza necessari per i sistemi operativi Windows in cui è in esecuzione l'applicazione client.
2.  Chiamare la funzione COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza predefinita per il processo in cui viene eseguita l'applicazione client. In questo modo viene dichiarata la sicurezza richiesta dalle altre applicazioni per accedere al processo in cui viene eseguita l'applicazione.
3.  Se è necessario modificare la sicurezza in un singolo proxy, ad esempio in un'altra chiamata a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), chiamare [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
4.  Se è necessario controllare l'hardware remoto o un oggetto di sistema che richiede un maggior numero di privilegi, utilizzare la funzione [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare i privilegi necessari. Si noti che non è possibile abilitare un privilegio a cui il processo non è già stato assegnato. Per ulteriori informazioni, vedere [controllo dell'accesso a oggetti privati](/windows/desktop/SecAuthZ/checking-access-to-private-objects).

Per ulteriori informazioni sull'impostazione del livello di sicurezza del processo predefinito, vedere Impostazione del livello di sicurezza [del processo predefinito mediante C++](setting-the-default-process-security-level-using-c-.md) e [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
