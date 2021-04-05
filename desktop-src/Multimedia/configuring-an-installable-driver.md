---
title: Configurazione di un driver installabile
description: Configurazione di un driver installabile
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- driver installabili, configurazione
- configurazione dei driver installabili
- OpenDriver (funzione)
- SendDriverMessage (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046574"
---
# <a name="configuring-an-installable-driver"></a>Configurazione di un driver installabile

Per indirizzare un driver installabile per eseguire attività utili, è necessario aprire il driver usando la funzione [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) e inviare i messaggi tramite la funzione [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) . Nell'esempio seguente viene illustrato come indirizzare il driver per visualizzare la relativa finestra di dialogo di configurazione.


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 