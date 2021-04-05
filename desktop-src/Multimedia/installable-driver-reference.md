---
title: Informazioni di riferimento sul driver installabile
description: Informazioni di riferimento sul driver installabile
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows Multimedia, Guida di riferimento per i driver installabili
- informazioni di riferimento sul driver installabile
- driver installabili, informazioni di riferimento
- informazioni di riferimento sul driver installabile, informazioni
- informazioni di riferimento per i driver installabili, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872373"
---
# <a name="installable-driver-reference"></a>Informazioni di riferimento sul driver installabile

Le funzioni e i messaggi associati a driver installabili sono raggruppati come indicato di seguito.

## <a name="loading-and-unloading-drivers"></a>Caricamento e scaricamento di driver

-   [GetDriverModuleHandle](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a>CloseDriver

-   [**\_chiusura DRV**](drv-close.md)
-   [**\_disabilitazione DRV**](drv-disable.md)
-   [**\_Abilitazione di DRV**](drv-enable.md)
-   [**DRV \_ disponibile**](drv-free.md)
-   [**\_caricamento DRV**](drv-load.md)
-   [**DRV \_ aperto**](drv-open.md)

## <a name="configuring-a-driver"></a>Configurazione di un driver

-   [**configurazione di DRV \_**](drv-configure.md)
-   [**\_QUERYCONFIGURE DRV**](drv-queryconfigure.md)
-   [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a>Installazione di un driver

-   [**installazione di DRV \_**](drv-install.md)
-   [**\_Rimuovi DRV**](drv-remove.md)

## <a name="driver-functions"></a>Funzioni driver

-   [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> </dl>

 

 