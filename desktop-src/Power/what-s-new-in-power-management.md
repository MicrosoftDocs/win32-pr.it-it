---
description: Windows 10 consente all'applicazione di ottimizzare il consumo di energia durante l'esecuzione in un dispositivo mobile.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novità del risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ac6ba320a98fce339f5bfacfe2d9b4a259be5a8150b2bcaabcac41179869e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143194"
---
# <a name="whats-new-in-power-management"></a>Novità di Risparmio energia

Windows 10 consente all'applicazione di ottimizzare il consumo di energia quando è in esecuzione in un dispositivo mobile.

## <a name="battery-saver"></a>Risparmia batteria

In questa versione, l'applicazione può ricevere una notifica quando risparmio batteria è attivata o disattivata. Rispondendo alle mutevoli condizioni di alimentazione, l'applicazione può collaborare con risparmio batteria per risparmiare energia ed estendere la durata della batteria. Per informazioni generali sulle risparmio batteria, vedere [risparmio batteria (nelle linee guida per i componenti hardware).](/windows-hardware/design/component-guidelines/battery-saver)

-   [**GUID \_ STATO \_ \_ RISPARMIO ENERGIA:**](power-setting-guids.md) usare questo nuovo GUID con la funzione [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) per ricevere una notifica quando risparmio batteria è attivata o disattivata.

-   [**SYSTEM \_ STATO \_ DI ALIMENTAZIONE:**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) questa struttura è stata aggiornata per supportare risparmio batteria. Il quarto membro, **SystemStatusFlag** (denominato in precedenza **Reserved1),** ora indica se risparmio batteria è attivato o meno. Usare la [**funzione GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) per recuperare un puntatore a questa struttura.

 

 
