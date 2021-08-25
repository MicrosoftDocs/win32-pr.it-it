---
title: Chiavi del Registro di sistema WCS
description: WCS usa le chiavi del Registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori. Le app devono eseguire query su queste chiavi del Registro di sistema per aggiornare lo stato del profilo colori del sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Sistema colori (WCS), chiavi del Registro di sistema
- WCS (Windows Color System), chiavi del Registro di sistema
- gestione dei colori delle immagini, chiavi del Registro di sistema
- gestione dei colori, chiavi del Registro di sistema
- colori, chiavi del Registro di sistema
- Informazioni di riferimento su WCS, chiavi del Registro di sistema
- informazioni di riferimento per WCS, chiavi del Registro di sistema
- Windows Sistema di colori (WCS), Registro di sistema
- WCS (Windows Color System),registro
- gestione dei colori delle immagini, Registro di sistema
- gestione dei colori, Registro di sistema
- colori, Registro di sistema
- Informazioni di riferimento su WCS, Registro di sistema
- informazioni di riferimento per WCS, Registro di sistema
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c12047d83ccc2f80c26521a59a040fa45df0c21e9bb035efff6ed5d38e8827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814351"
---
# <a name="wcs-registry-keys"></a>Chiavi del Registro di sistema WCS

WCS usa le chiavi del Registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori. Le app devono eseguire query su queste chiavi del Registro di sistema per aggiornare lo stato del profilo colori del sistema.

## <a name="active-color-profile-changed"></a>Profilo colori attivo modificato

Le app potrebbero voler rispondere agli eventi di modifica del profilo colori per un dispositivo di monitoraggio. in modo da avere sempre informazioni accurate sul colore per la destinazione, anche se l'utente o un'altra app ha modificato il profilo attivo per il dispositivo.

### <a name="desktop-applications"></a>Applicazioni desktop

Le app desktop devono restare in ascolto delle modifiche apportate al Registro di sistema per determinare quando sono state modificate le associazioni di un profilo colori tramite [**RegNotifyChangeKeyValue.**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) Un'app deve registrare sia per le modifiche di associazione del profilo per utente che per le modifiche a livello di sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve essere inizializzato con una chiave HKEY fornita da [**RegOpenKeyEx.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) **RegOpenKeyEx** deve essere inizializzato usando i percorsi dell'albero del Registro di sistema seguenti:



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Associazioni di profili per utente    | **HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion ICM \\ \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| Associazioni di profili a livello di sistema | **Classe di controllo HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

Quando l'app viene avvisata di una modifica della chiave del Registro di sistema, deve prima di tutto eseguire una query se le associazioni per utente o a livello di sistema vengono usate chiamando [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). Deve quindi chiamare [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) con il valore [**WCS \_ PROFILE MANAGEMENT \_ \_ SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) per ottenere il nuovo profilo colori attivo per il monitoraggio. Si noti che non tutte le modifiche della chiave del Registro di sistema corrisponderanno a una modifica effettiva nel profilo colori attualmente attivo. l'app mush controlla se il profilo restituito da **WcsGetDefaultColorProfile è** stato effettivamente modificato.

### <a name="universal-windows-uwp-apps"></a>App UWP (Universal Windows)

Le Windows universali non hanno accesso alle chiavi del Registro di sistema precedenti. Devono invece registrare un gestore per [**l'evento DisplayInformation.ColorProfileChanged.**](/uwp/api/Windows.Graphics.Display.DisplayInformation) Questo evento viene generato ogni volta che il profilo colori attivo per il monitoraggio in cui è in esecuzione l'applicazione viene modificato. ColorProfileChanged tiene conto dell'uso delle associazioni di profili per utente o a livello di sistema. queste informazioni vengono astratte dalle app UWP.

Quando risponde all'evento ColorProfileChanged, l'app deve eseguire una query sul profilo attualmente attivo usando [**DisplayInformation.GetColorProfileAsync.**](/uwp/api/Windows.Graphics.Display.DisplayInformation)

 

 