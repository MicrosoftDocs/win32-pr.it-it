---
description: "Se si usa l'API COM per WMI per recuperare o archiviare le informazioni sulle classi localizzate, specificare le impostazioni locali nel parametro strLocale per l'interfaccia IWbemLocator:: ConnectServer."
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recupero di classi modificate tramite l'API COM per WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759761"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Recupero di classi modificate tramite l'API COM per WMI

Se si usa l'API COM per WMI per recuperare o archiviare le informazioni sulle classi localizzate, specificare le impostazioni locali nel parametro *strLocale* per l'interfaccia [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . Durante la lettura o la scrittura di classi modificate, indicare che si desidera utilizzare le definizioni di classe localizzate specificando \_ il flag WBEM \_ utilizzare \_ \_ i qualificatori modificati come flag per il parametro *iFlags* .

Nella tabella seguente sono elencate le versioni sincrone e asincrone dei metodi che usano il flag WBEM usare il flag di \_ \_ \_ \_ qualificatori modificati.



| Metodo sincrono                                                            | Metodo asincrono                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



