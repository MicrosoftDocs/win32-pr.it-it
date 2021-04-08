---
description: comma/datamode/dial out
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: comma/datamode/dial out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967987"
---
# <a name="commdatamodemdialout"></a>comma/datamode/dial out

La classe di dispositivi **comm/DataModel/Dial** out è costituita da dispositivi DataModel utilizzati solo per le chiamate in uscita. Questa classe sostituisce la classe [**comm/DataModel**](comm-datamodem.md) nei sistemi operativi Windows 2000 e versioni successive.

Prima di Windows 2000, il TSP Unimodem supportava solo la classe del dispositivo [**comm/DataModel**](comm-datamodem.md) . È possibile che si verifichi un comportamento imprevisto quando un'applicazione che compone una chiamata in uscita modifica il set di configurazione da parte di un servizio in attesa di una chiamata in ingresso. Le applicazioni che usano sistemi operativi Windows 2000 e versioni successive devono specificare [**comm/datamodet/dialin**](comm-datamodem-dialin.md) o **comm/datamode/Dial** out nelle chiamate a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) o [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Questo consente a UniModel di mantenere una configurazione di connessione remota indipendente dalla configurazione di connessione remota.

Anche se **comm/DataModel/Dial** out viene usato da UNIMODE in Windows 2000 e versioni successive, può essere usato anche da altri TSPs su qualsiasi piattaforma. Le applicazioni che devono essere eseguite in tutte le piattaforme devono prima usare **comm/datamode/Dial** out nelle chiamate all'API che richiedono una classe Device e usano solo [**comm/datamodet**](comm-datamodem.md) se l'API restituisce **LINEERR \_ INVALCALLSTATE**.

Il provider di servizi Unimodem converte la classe di dispositivi [**comm/DataModel**](comm-datamodem.md) nelle chiamate a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) a [**comm/DataModel/dialin**](comm-datamodem-dialin.md) o a comm/datamodet **/Dialing** , come indicato di seguito:

-   Windows 2000 e versioni successive:
    -   Se viene specificato **null** nel parametro *lpszDeviceClass* nella chiamata a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), unimodeism presuppone [**comm/DataModel/dialin**](comm-datamodem-dialin.md). Se si specifica [**comm/DataModel**](comm-datamodem.md) o [**TAPI/Line**](tapi-line.md) nella chiamata a **lineConfigDialog**, UniModel converte questo oggetto in **comm/datamodet/Dial** out.
    -   Nella chiamata a [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) o [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**comm/datamode**](comm-datamodem.md) è gestito come **comm/datamode/Dial** out. **Null** indica una classe di dispositivo non valida.
-   Prima di Windows 2000:
    -   Se si specifica **null** o [**TAPI/line**](tapi-line.md) in [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), UNIMODE è il [**Metodo comm/DataModel**](comm-datamodem.md).

La classe **comm/DataModel/Dial** out usa le strutture e le configurazioni descritte nella classe del dispositivo [**comm/DataModel**](comm-datamodem.md) .

 

 



