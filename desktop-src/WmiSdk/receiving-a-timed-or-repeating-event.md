---
description: Un evento temporizzato o ripetuto è un evento che si verifica in un'ora e una data specifiche o ripetutamente a intervalli regolari. Ad esempio, un evento può verificarsi a mezzanotte solo il 2 dicembre 2015 o una volta ogni settimana il martedì alle 2:31 PM.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Ricezione di un evento temporizzato o ripetuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226837"
---
# <a name="receiving-a-timed-or-repeating-event"></a>Ricezione di un evento temporizzato o ripetuto

Un evento temporizzato o ripetuto è un evento che si verifica in un'ora e una data specifiche o ripetutamente a intervalli regolari. Ad esempio, un evento può verificarsi a mezzanotte solo il 2 dicembre 2015 o una volta ogni settimana il martedì alle 2:31 PM.

La tabella seguente elenca le diverse classi usate per creare un evento temporizzato o ripetuto.



| Classe                                                                                            | Descrizione                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [ **\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | Modello di eventi Microsoft standard.<br/> Per ulteriori informazioni, vedere [creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).<br/> |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                               | Tecnica legacy.<br/> Per ulteriori informazioni, vedere [creazione di un evento timer con \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).<br/>                                             |



 

Se si desidera pianificare l'esecuzione di un'attività o di un processo in un momento specifico o ripetutamente, utilizzare la classe [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) e i relativi metodi. Questa classe rappresenta un processo creato con il comando AT in una finestra di comando da **Start** , quindi da **eseguire** o dalle **attività pianificate** nel **Pannello di controllo**.

 

