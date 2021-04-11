---
title: Interfaccia IWMDRMDeviceApp2
description: L'interfaccia IWMDRMDeviceApp2 estende IWMDRMDeviceApp fornendo una nuova versione del metodo QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interfaccia IWMDRMDeviceApp2 Windows Media Gestione dispositivi
- Interfaccia IWMDRMDeviceApp2 Windows Media Gestione dispositivi, descritta
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334807"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interfaccia IWMDRMDeviceApp2

L'interfaccia **IWMDRMDeviceApp2** estende [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) fornendo una nuova versione del metodo [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) . **QueryDeviceStatus2** consente al chiamante di eseguire una query per un requisito DRM specifico.

Per ottenere questa interfaccia, chiamare **CoCreateInstance** e passare il CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Questa interfaccia viene definita nel file di intestazione compilato da WMDRMDeviceApp. idl. Questa intestazione **\# include** "WMDM. h". Potrebbe essere necessario modificare il nome del file in modo che corrisponda all'intestazione compilata da WMDM. idl.

 

## <a name="members"></a>Membri

L'interfaccia **IWMDRMDeviceApp2** eredita da [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IWMDRMDeviceApp2** dispone di questi metodi.



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

 

 





