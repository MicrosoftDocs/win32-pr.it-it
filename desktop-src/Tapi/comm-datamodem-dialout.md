---
description: comm/datamodem/dialout
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: comm/datamodem/dialout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c8c3ecbe81c5e63b8a8ccd820e306cbfe8f7ed4ab60b4252fbf6d0b8c07c06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118868109"
---
# <a name="commdatamodemdialout"></a>comm/datamodem/dialout

La **classe di dispositivo comm/datamodem/dialout** è costituita da dispositivi datamodem usati solo per le chiamate in uscita. Questa classe sostituisce la [**classe comm/datamodem**](comm-datamodem.md) Windows 2000 e versioni successive.

Prima Windows 2000, il TSP Unimodem supportava solo la classe di dispositivo [**comm/datamodem.**](comm-datamodem.md) Un comportamento imprevisto può verificarsi quando un'applicazione che chiama una chiamata in uscita modifica la configurazione impostata da un servizio in attesa di una chiamata in ingresso. Le applicazioni che usano Windows 2000 e versioni successive devono specificare [**comm/datamodem/dialin**](comm-datamodem-dialin.md) o **comm/datamodem/dialout** nelle chiamate a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) o [**lineSetDevConfig.**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) Ciò consente a Unimodem di mantenere una configurazione dial-in indipendente dalla configurazione dial-out.

Anche se **comm/datamodem/dialout** viene usato da Unimodem in Windows 2000 e versioni successive, può essere usato anche da altri TSP in qualsiasi piattaforma. Le applicazioni che devono essere eseguite in tutte le piattaforme devono prima usare **comm/datamodem/dialout** nelle chiamate all'API che richiedono una classe di dispositivo e usare [**comm/datamodem solo**](comm-datamodem.md) se l'API restituisce **LINEERR \_ INVALCALLSTATE.**

Il provider di servizi Unimodem converte la classe di dispositivo [**comm/datamodem**](comm-datamodem.md) nelle chiamate [**a lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) e [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) in [**comm/datamodem/dialin**](comm-datamodem-dialin.md) o **comm/datamodem/dialout** come indicato di seguito:

-   Windows 2000 e versioni successive:
    -   Se **viene** specificato NULL nel parametro *lpszDeviceClass* nella chiamata a [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem presuppone [**comm/datamodem/dialin**](comm-datamodem-dialin.md). Se [**si specifica comm/datamodem**](comm-datamodem.md) o [**tapi/line**](tapi-line.md) nella chiamata a **lineConfigDialog**, Unimodem lo converte in **comm/datamodem/dialout.**
    -   Nella chiamata a [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) o [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig), [**comm/datamodem**](comm-datamodem.md) viene gestito come **comm/datamodem/dialout.** **NULL** indica una classe di dispositivo non valida.
-   Prima Windows 2000:
    -   Se si **specifica NULL** [**o tapi/line**](tapi-line.md) in [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog), Unimodem presuppone [**comm/datamodem**](comm-datamodem.md).

La **classe comm/datamodem/dialout** usa le strutture e le configurazioni descritte nella classe di dispositivo [**comm/datamodem.**](comm-datamodem.md)

 

 



