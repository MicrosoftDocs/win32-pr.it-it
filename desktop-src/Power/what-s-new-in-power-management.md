---
description: Windows 10 consente all'applicazione di ottimizzare il consumo di energia quando è in esecuzione in un dispositivo mobile.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novità del risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312006"
---
# <a name="whats-new-in-power-management"></a>Novità di Risparmio energia

Windows 10 consente all'applicazione di ottimizzare il consumo di energia quando viene eseguito in un dispositivo mobile.

## <a name="battery-saver"></a>Risparmia batteria

In questa versione, l'applicazione può ricevere una notifica quando lo screen saver è attivato o disattivato. Rispondendo alle mutevoli condizioni di alimentazione, l'applicazione può collaborare con lo screen saver per risparmiare energia e contribuire a estendere la durata della batteria. Per informazioni generali sul risparmio di batteria, vedere [batteria saver (nelle linee guida del componente hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ \_ \_ Stato risparmio energia**](power-setting-guids.md) : usare questo nuovo GUID con la funzione [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) per ricevere una notifica quando lo screen saver della batteria è attivato o disattivato.

-   [**Sistema \_ di \_Stato di alimentazione**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : questa struttura è stata aggiornata per supportare il risparmio di batterie. Il quarto membro, **SystemStatusFlag** (denominato in precedenza **Reserved1**), ora indica se il risparmio di batteria è impegnato o meno. Utilizzare la funzione [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) per recuperare un puntatore a questa struttura.

 

 
