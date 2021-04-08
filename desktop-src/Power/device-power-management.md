---
description: L'API per la potenza del dispositivo consente di determinare facilmente quali dispositivi sono in grado di riattivare il sistema da uno stato di sospensione e quali Stati di sospensione supportano il risveglio dei dispositivi. Per ulteriori informazioni sugli stati di sospensione, vedere la pagina relativa agli Stati di alimentazione del sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Risparmio energia del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967498"
---
# <a name="device-power-management"></a>Risparmio energia del dispositivo

L'API per la potenza del dispositivo consente di determinare facilmente quali dispositivi sono in grado di riattivare il sistema da uno stato di sospensione e quali Stati di sospensione supportano il risveglio dei dispositivi. Per ulteriori informazioni sugli stati di sospensione, vedere la pagina relativa [agli Stati di alimentazione del sistema](system-power-states.md).

La funzione [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) può essere usata per eseguire ricerche nell'elenco dei dispositivi che soddisfano i criteri specificati. I criteri possono includere la capacità del dispositivo di supportare uno stato del sistema o riattivare da tale stato. I flag attualmente supportati sono reperibili in WinNT. h e DevPower. h.

La funzione [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) Abilita o Disabilita un dispositivo specificato per riattivare il sistema da uno stato di sospensione.

L'API per l'alimentazione del dispositivo consente agli sviluppatori di creare un'esperienza utente migliore offrendo all'utente informazioni aggiuntive sulle operazioni svolte dal sistema e un maggiore controllo sui dispositivi nel sistema. La potenza del dispositivo è utile nelle situazioni in cui il consumo di energia è fondamentale, ad esempio nei dispositivi portatili in esecuzione sulle batterie. Ad esempio, lo schema di risparmio energia usato in un computer desktop potrebbe non essere lo schema ottimale per un computer portatile, quindi è possibile che l'utente desideri disabilitare la riattivazione del sistema da parte di alcuni dispositivi. In questo modo è possibile ridurre l'energia perché i dispositivi disabilitati non risulteranno più potenti quando il sistema è in modalità sospensione.

Per un esempio, vedere [uso dell'API per la potenza del dispositivo](using-the-device-power-api.md).

 

 



