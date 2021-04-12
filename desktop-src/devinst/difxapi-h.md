---
title: Difxapi.h
description: Questa sezione contiene argomenti di riferimento per l'intestazione difxapi. h.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c549ed3fd781d9fde4e6ab48703e1df425986d0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223931"
---
# <a name="difxapih"></a>Difxapi.h

Questa sezione contiene argomenti di riferimento per l'intestazione difxapi. h.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DIFLOGCALLBACK*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | Una funzione tipizzata in **DIFLOGCALLBACK** è una funzione di callback fornita dall'applicazione che un'applicazione registra chiamando [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback). DIFxAPI chiama la funzione di callback per registrare gli eventi che si verificano durante l'operazione DIFxAPI.<br/>                        |
| [*DIFXAPILOGCALLBACK*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | Una funzione tipizzata in **DIFXAPILOGCALLBACK** è una funzione di callback fornita dall'applicazione che un'applicazione registra con difxapi chiamando [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback). DIFxAPI chiama la funzione di callback per registrare gli eventi che si verificano durante l'operazione DIFxAPI.<br/> |
| [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | La funzione **DIFXAPISetLogCallback** registra una funzione di callback fornita dal chiamante che difxapi chiama per registrare informazioni sugli eventi che si verificano durante le operazioni difxapi. <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | La funzione **DriverPackageGetPath** Recupera il percorso completo del [file inf](/windows-hardware/drivers/install/overview-of-inf-files) per un [pacchetto di driver](/windows-hardware/drivers/install/driver-packages)preinstallato.<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | La funzione **DriverPackageInstall** preinstalla un [pacchetto driver](/windows-hardware/drivers/install/driver-packages) , quindi installa il driver nel sistema.<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | La funzione **DriverPackagePreinstall** preinstalla un [pacchetto driver](/windows-hardware/drivers/install/driver-packages) per un [driver della funzione](/windows-hardware/drivers/kernel/function-drivers) plug and Play (PNP) e installa il [file inf](/windows-hardware/drivers/install/overview-of-inf-files) per il pacchetto driver nella directory dei file di sistema inf.<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | La funzione **DriverPackageUninstall** Disinstalla il [pacchetto driver](/windows-hardware/drivers/install/driver-packages) specificato dal sistema e rimuove il pacchetto driver. <br/>                                                                                                                               |
| [**INSTALLERINFO**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | La struttura INSTALLERINFO contiene informazioni su un'applicazione che DIFxAPI associa a un [pacchetto driver](/windows-hardware/drivers/install/driver-packages). <br/>                                                                                                                                          |
| [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | La funzione **SetDifxLogCallback** registra una funzione di callback fornita dal chiamante che difxapi chiama per registrare informazioni sugli eventi che si verificano durante le operazioni difxapi. <br/>                                                                                                               |



 

 

 

[Invia commenti su questo argomento a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Invia commenti su questo argomento a Microsoft")