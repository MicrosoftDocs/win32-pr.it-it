---
description: Sono presenti nove operazioni asincrone correlate ai telefoni.
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: Operazioni del telefono asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883242"
---
# <a name="asynchronous-phone-operations"></a>Operazioni del telefono asincrone

Sono presenti nove operazioni asincrone correlate ai telefoni. Queste vengono avviate dalle funzioni [**TSPI \_ phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI \_ phoneSetData**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata), TSPI phoneSetDisplay, TSPI [**phoneSetGain \_**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch) [**phoneSetHookSwitch, TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain)phoneSetLamp, TSPI [**phoneSetRing e \_**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp) [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) . [**\_**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring) Se un'applicazione chiama la funzione TAPI [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) e dispone dell'unico handle per il telefono, TAPI chiama la funzione [**TSPI \_ phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) per indicare al provider di servizi di terminare le operazioni asincrone e chiamare la funzione di callback [*\_ proc proc*](/windows/win32/api/tspi/nc-tspi-async_completion) come appropriato. Se l'applicazione non dispone dell'unico handle per il telefono, il provider di servizi non riceve alcuna notifica della richiesta e tutte le operazioni asincrone in attesa rimangono attive.

 

 
