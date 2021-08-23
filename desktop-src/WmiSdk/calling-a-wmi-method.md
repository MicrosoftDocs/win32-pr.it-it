---
title: Come chiamare un metodo WMI
description: Lo scopo principale di WMI è fornire l'accesso a classi e istanze che rappresentano oggetti nella rete.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1de14f06388454228528d5a419b551ae2ed0d72c82e3b78c9e04855db6619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051049"
---
# <a name="how-to-call-a-wmi-method"></a>Come chiamare un metodo WMI

Lo scopo principale di WMI è fornire l'accesso a classi e istanze che rappresentano oggetti nella rete. Queste classi e istanze sono supportate dai provider. Ad esempio, tutte le istanze che rappresentano dispositivi hardware standard nell'azienda, ad esempio [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) o [**Win32 \_ Printer,**](/windows/desktop/CIMWin32Prov/win32-printer)sono supportate dal provider Win32. Analogamente, è possibile accedere al registro eventi tramite il provider del registro eventi e al Registro di sistema tramite il provider del Registro di sistema.

I metodi implementati da WMI in interfacce come [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) o oggetti di scripting, ad esempio [**SWbemServices**](swbemservices.md), sono principalmente per ottenere e modificare in modo generico i dati forniti da qualsiasi provider. Ad esempio, usare [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) per ottenere tutte le istanze del processo [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) in un subset di computer aziendali. È quindi possibile chiamare il metodo del provider Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) su ogni **oggetto Processo Win32. \_**

Nell'esempio seguente il [**metodo GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) viene chiamato come metodo di automazione nell'oggetto Process. Un metodo WMI, ad esempio il [**metodo \_ Path**](swbemobject-path-.md) definito per [**SWbemObject,**](swbemobject.md) può essere chiamato anche sull'oggetto **Process.**


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



Il processo effettivo di utilizzo dei metodi WMI è identico all'uso di qualsiasi altro Windows COM o dell'interfaccia di automazione. Per altre informazioni, vedere [COM](../cossdk/component-services-portal.md) e [Creazione di un'applicazione WMI o di uno script](creating-a-wmi-application-or-script.md). Per altre informazioni sulle interfacce supportate da WMI, vedere [API COM per WMI](com-api-for-wmi.md) e API di scripting per [WMI](scripting-api-for-wmi.md).

Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamata di un metodo](calling-a-method.md)
</dt> </dl>

 

 
