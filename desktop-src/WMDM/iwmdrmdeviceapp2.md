---
title: Interfaccia IWMDRMDeviceApp2
description: L'interfaccia IWMDRMDeviceApp2 estende IWMDRMDeviceApp fornendo una nuova versione del metodo QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interfaccia IWMDRMDeviceApp2 windows Media Device Manager
- Interfaccia IWMDRMDeviceApp2 windows Media Device Manager , descritta
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17bd0d7aa729103a81fca6732ed178ac5ced583566dd353a28716d4933e602ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584495"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interfaccia IWMDRMDeviceApp2

**L'interfaccia IWMDRMDeviceApp2** estende [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) fornendo una nuova versione del [**metodo QueryDeviceStatus.**](iwmdrmdeviceapp-querydevicestatus.md) **QueryDeviceStatus2** consente al chiamante di eseguire una query per un requisito DRM specifico.

Per ottenere questa interfaccia, chiamare **CoCreateInstance** e passare CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Questa interfaccia è definita nel file di intestazione compilato da WMDRMDeviceApp.idl. Questa intestazione **\# include** "wmdm.h". Potrebbe essere necessario modificare questo nome file in modo che corrisponda all'intestazione compilata da WMDM.idl.

 

## <a name="members"></a>Membri

**L'interfaccia IWMDRMDeviceApp2** eredita da [**IWMDRMDeviceApp.**](iwmdrmdeviceapp.md) **IWMDRMDeviceApp2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IWMDRMDeviceApp2** include questi metodi.



| Metodo                                                            | Descrizione                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Esegue una query su un dispositivo per uno stato o una funzionalità DRM specifica.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Gestione del contenuto protetto nell'applicazione**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfacce per le applicazioni**](interfaces-for-applications.md)
</dt> <dt>

[**Misurazione dell'utilizzo del contenuto**](metering-content-usage.md)
</dt> </dl>

 

 





