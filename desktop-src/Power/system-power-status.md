---
description: Lo stato di alimentazione del sistema indica se l'origine di alimentazione per un computer è una batteria di sistema o un alimentatore AC. Per i computer che utilizzano batterie, lo stato di alimentazione del sistema indica anche la quantità di durata della batteria e l'eventuale ricarica della batteria.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Stato di alimentazione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312013"
---
# <a name="system-power-status"></a>Stato di alimentazione del sistema

Lo stato di alimentazione del sistema indica se l'origine di alimentazione per un computer è una batteria di sistema o un alimentatore AC. Per i computer che utilizzano batterie, lo stato di alimentazione del sistema indica anche la quantità di durata della batteria e l'eventuale ricarica della batteria.

Le informazioni di risparmio energia vengono recuperate eseguendo la registrazione per le notifiche di impostazioni di risparmio energia tramite la funzione [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Questa funzione consente alle applicazioni di eseguire la registrazione per impostazioni di risparmio energia specifiche e ricevere notifiche quando cambiano.

> [!Note]  
> Per eseguire una query per ottenere informazioni sullo stato dell'alimentazione senza notifiche, usare [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).

 

Le applicazioni e i driver installabili usano in genere lo stato di alimentazione del sistema per determinare se è possibile eseguire l'operazione continua. Ad esempio, prima che un'applicazione esegua operazioni in background, ad esempio la compressione o la paginazione di un file, deve controllare se il sistema è su batterie. Come altro esempio, un'applicazione che sta iniziando un'operazione di lunga durata deve controllare lo stato per determinare se è disponibile una quantità sufficiente di energia elettrica per completare l'operazione.

Per impostazione predefinita, il sistema non esegue query su applicazioni o driver durante le transizioni di sospensione.

> [!Note]  
> Se il risparmio di energia è basso, un'applicazione può richiedere l'intervento dell'utente o richiedere che il sistema si sospenda automaticamente. È possibile sospendere l'operazione di sistema utilizzando la funzione [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>

 

 



