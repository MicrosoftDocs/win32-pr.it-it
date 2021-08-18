---
title: Informazioni di riferimento sul driver installabile
description: Informazioni di riferimento sul driver installabile
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows informazioni di riferimento sul driver multimediale e installabile
- informazioni di riferimento sul driver multimediali e installabili
- driver installabili, informazioni di riferimento
- informazioni di riferimento sui driver installabili, informazioni su
- informazioni di riferimento sui driver installabili, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dd2488f0b07805edbcdc90187309db2a04c9c0ced4f4b5b0af4e50bd983ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038641"
---
# <a name="installable-driver-reference"></a>Informazioni di riferimento sul driver installabile

Le funzioni e i messaggi associati ai driver installabili sono raggruppati come indicato di seguito.

## <a name="loading-and-unloading-drivers"></a>Caricamento e scaricamento dei driver

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**DRV \_ CLOSE**](drv-close.md)
-   [**DISABILITAZIONE \_ DRV**](drv-disable.md)
-   [**DRV \_ ENABLE**](drv-enable.md)
-   [**DRV \_ GRATUITO**](drv-free.md)
-   [**CARICAMENTO \_ DRV**](drv-load.md)
-   [**DRV \_ OPEN**](drv-open.md)

## <a name="configuring-a-driver"></a>Configurazione di un driver

-   [**CONFIGURAZIONE \_ DRV**](drv-configure.md)
-   [**QUERY \_ DRVCONFIGURARE**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>Installazione di un driver

-   [**INSTALLAZIONE DI \_ DRV**](drv-install.md)
-   [**RIMOZIONE DI \_ DRV**](drv-remove.md)

## <a name="driver-functions"></a>Funzioni del driver

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> </dl>

 

 