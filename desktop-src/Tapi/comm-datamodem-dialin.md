---
description: comm/datamode/dialin
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: comm/datamode/dialin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb66d72b5d9f2c75af361153d46f5cac9abdfd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967988"
---
# <a name="commdatamodemdialin"></a>comm/datamode/dialin

La classe del dispositivo **comm/DataModel/dialin** è costituita da dispositivi DataModel utilizzati solo per le chiamate in ingresso. Questa classe sostituisce la classe [**comm/DataModel**](comm-datamodem.md) nei sistemi operativi Windows 2000 e versioni successive.

Prima di Windows 2000, il TSP Unimodem supportava solo la classe del dispositivo [**comm/DataModel**](comm-datamodem.md) . È possibile che si verifichi un comportamento imprevisto quando un'applicazione che compone una chiamata in uscita modifica il set di configurazione da parte di un servizio in attesa di una chiamata in ingresso. Le applicazioni che usano sistemi operativi Windows 2000 e versioni successive devono specificare **comm/datamodet/dialin** o [**comm/datamode/Dial**](comm-datamodem-dialout.md) out nelle chiamate a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) o [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig). Questo consente a UniModel di mantenere una configurazione di connessione remota indipendente dalla configurazione di connessione remota.

Anche se **comm/DataModel/dialin** viene usato da UNIMODE in Windows 2000 e versioni successive, può essere usato anche da altri TSPs su qualsiasi piattaforma. Le applicazioni che devono essere eseguite in tutte le piattaforme devono prima usare **comm/datamode/dialin** nelle chiamate alle API che richiedono una classe Device e usano solo [**comm/datamodet**](comm-datamodem.md) se l'API restituisce **LINEERR \_ INVALCALLSTATE**.

Il provider di servizi Unimodem converte la classe di dispositivi [**comm/DataModel**](comm-datamodem.md) nelle chiamate a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) a **comm/DataModel/dialin** o a comm/datamodet [**/Dialing**](comm-datamodem-dialout.md) , come indicato di seguito:

-   Windows 2000 e versioni successive:
    -   Se viene specificato **null** nel parametro *lpszDeviceClass* nella chiamata a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), unimodeism presuppone **comm/DataModel/dialin**. Se si specifica [**comm/DataModel**](comm-datamodem.md) o [**TAPI/Line**](tapi-line.md) nella chiamata a **lineConfigDialog**, UniModel converte questo oggetto in [**comm/datamodet/Dial**](comm-datamodem-dialout.md)out.
    -   Nella chiamata a [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) o [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**comm/datamode**](comm-datamodem.md) è gestito come [**comm/datamode/Dial**](comm-datamodem-dialout.md)out. **Null** indica una classe di dispositivo non valida.
-   Prima di Windows 2000:
    -   Se si specifica **null** o [**TAPI/line**](tapi-line.md) in [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), UNIMODE è il [**Metodo comm/DataModel**](comm-datamodem.md).

La classe **comm/DataModel/dialin** usa le strutture e le configurazioni descritte nella classe del dispositivo [**comm/DataModel**](comm-datamodem.md) .

 

 



