---
description: Le applicazioni client che chiamano interfacce WMI possono controllare i livelli di sicurezza dei processi.
ms.assetid: 790b4e40-9b92-464a-a774-dec0b75cedee
ms.tgt_platform: multiple
title: Impostazione della sicurezza del processo dell'applicazione client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be6b3f6e632ade53700bbe81afc7698a06fe2ff038e0c57c1b4a7eed44afa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739472"
---
# <a name="setting-client-application-process-security"></a>Impostazione della sicurezza del processo dell'applicazione client

Le applicazioni client che chiamano interfacce WMI possono controllare i livelli di sicurezza dei processi. Tutte le applicazioni WMI accedono a WMI tramite COM ed è possibile chiamare la funzione COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza per i processi. Le applicazioni che effettuano chiamate asincrone a WMI e le applicazioni registrate come consumer di eventi impostano i livelli di sicurezza nella chiamata a WMI.

Se non si effettua una chiamata esplicita a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM la chiama in modo implicito con i valori del Registro di sistema. Tuttavia, i valori del Registro di sistema possono avere impostazioni inferiori per la rappresentazione e l'autenticazione che non forniscono la sicurezza necessaria per WMI. Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite C++.](setting-the-default-process-security-level-using-c-.md)

L'accesso asincrono a WMI non è consigliato. Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semisincrono o sincrona oppure eseguire controlli di accesso adeguati nell'applicazione client. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Le chiamate a uno dei proxy WMI ([**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject),[**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)o [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)) usano un puntatore out-of-process. Per altre informazioni sulle impostazioni predefinite e le raccomandazioni, vedere Impostazione della sicurezza in [IWbemServices e altri proxy.](setting-the-security-on-iwbemservices-and-other-proxies.md)

La procedura seguente descrive i passaggi da eseguire per impostare la sicurezza per WMI nel processo dell'applicazione.

**Per impostare la sicurezza per WMI nel processo dell'applicazione**

1.  Determinare i livelli di sicurezza necessari per Windows sistemi operativi in cui viene eseguita l'applicazione client.
2.  Chiamare la funzione [**COM CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza predefinita per il processo in cui viene eseguita l'applicazione client. In questo modo viene dichiarata la quantità di sicurezza necessaria ad altre applicazioni per accedere al processo in cui viene eseguita l'applicazione.
3.  Se è necessario modificare la sicurezza in un singolo proxy, ad esempio in un'altra chiamata a [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)chiamare [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)
4.  Se è necessario controllare l'hardware remoto o un oggetto di sistema che richiede più privilegi, usare la [**funzione AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per abilitare i privilegi necessari. Si noti che non è possibile abilitare un privilegio a cui il processo non è già stato assegnato. Per altre informazioni, vedere [Controllo dell'accesso agli oggetti privati.](/windows/desktop/SecAuthZ/checking-access-to-private-objects)

Per altre informazioni sull'impostazione del livello di sicurezza del processo predefinito, vedere Impostazione del livello di sicurezza del processo predefinito tramite [C++](setting-the-default-process-security-level-using-c-.md) e Impostazione del livello di sicurezza del processo predefinito [tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

 

 
