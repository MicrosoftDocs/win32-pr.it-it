---
title: Come chiamare un metodo WMI
description: Lo scopo principale di WMI è fornire l'accesso alle classi e alle istanze che rappresentano gli oggetti nella rete.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529556"
---
# <a name="how-to-call-a-wmi-method"></a>Come chiamare un metodo WMI

Lo scopo principale di WMI è fornire l'accesso alle classi e alle istanze che rappresentano gli oggetti nella rete. Queste classi e istanze sono supportate dai provider. Ad esempio, tutte le istanze che rappresentano i dispositivi hardware standard nell'azienda, ad esempio [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) o la [**\_ stampante Win32**](/windows/desktop/CIMWin32Prov/win32-printer), sono supportate dal provider Win32. Analogamente, è possibile accedere al registro eventi tramite il provider del registro eventi e il registro di sistema tramite il provider del registro di sistema.

I metodi implementati da WMI nelle interfacce, ad esempio [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o gli oggetti di scripting come [**SWbemServices**](swbemservices.md), sono principalmente per ottenere e modificare in modo generico i dati forniti da qualsiasi provider. Ad esempio, usare [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) per ottenere tutte le istanze del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) in un subset di computer aziendali. È quindi possibile chiamare il metodo del provider Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) in ogni oggetto **\_ processo Win32** .

Nell'esempio seguente, il metodo [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) viene chiamato come metodo di automazione nell'oggetto Process. Un metodo WMI, ad esempio il [**metodo \_ path**](swbemobject-path-.md) definito per [**SWbemObject**](swbemobject.md) , può essere chiamato anche sull'oggetto **Process** .


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



Il processo effettivo di utilizzo dei metodi WMI è identico all'utilizzo di qualsiasi altra interfaccia COM o di automazione di Windows. Per ulteriori informazioni, vedere [com](../cossdk/component-services-portal.md) e [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md). Per ulteriori informazioni sulle interfacce supportate da WMI, vedere [API com per WMI](com-api-for-wmi.md) e [API di scripting per WMI](scripting-api-for-wmi.md).

Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata a un metodo](calling-a-method.md)
</dt> </dl>

 

 
