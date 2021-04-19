---
title: Chiavi del registro di sistema WCS
description: WCS usa le chiavi del registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori. Le app devono eseguire una query su queste chiavi del registro di sistema per aggiornare lo stato del profilo colori
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), chiavi del registro di sistema
- WCS (sistema di colori Windows), chiavi del registro di sistema
- Gestione colori immagine, chiavi del registro di sistema
- gestione dei colori, chiavi del registro di sistema
- colori, chiavi del registro di sistema
- Riferimento a WCS, chiavi del registro di sistema
- informazioni di riferimento su WCS, chiavi del registro di sistema
- Windows Color System (WCS), registro di sistema
- WCS (sistema di colori Windows), registro di sistema
- Gestione colori immagine, registro di sistema
- gestione dei colori, registro di sistema
- colori, registro di sistema
- Riferimento a WCS, registro di sistema
- informazioni di riferimento su WCS, registro di sistema
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320204"
---
# <a name="wcs-registry-keys"></a>Chiavi del registro di sistema WCS

WCS usa le chiavi del registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori. Le app devono eseguire una query su queste chiavi del registro di sistema per aggiornare lo stato del profilo colori

## <a name="active-color-profile-changed"></a>Profilo colore attivo modificato

Le app potrebbero voler rispondere agli eventi di modifica del profilo colori per un dispositivo di monitoraggio; in questo modo si garantisce che siano sempre disponibili informazioni accurate sui colori per la destinazione, anche se l'utente o un'altra app ha modificato il profilo attivo per il dispositivo.

### <a name="desktop-applications"></a>Applicazioni desktop

Le applicazioni desktop devono restare in ascolto delle modifiche al registro di sistema per determinare quando le associazioni del profilo colori sono state modificate usando [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue). Un'app deve registrarsi sia per le modifiche dell'associazione del profilo per utente che per le modifiche a livello di sistema.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve essere inizializzato con un HKEY fornito da [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa). **RegOpenKeyEx** deve essere inizializzato utilizzando i seguenti percorsi dell'albero del registro di sistema:



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Associazioni di profili per utente    | **HKEY \_ \_ software utente corrente \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ display \\ {4D36E96E-E325-11CE-BFC1-08002BE10318}** |
| Associazioni profilo a livello di sistema | **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Class \\ {4D36E96E-E325-11CE-BFC1-08002BE10318}**                                        |



 

Quando l'app riceve una notifica di una modifica della chiave del registro di sistema, deve prima eseguire una query se le associazioni per utente o a livello di sistema vengono utilizzate chiamando [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent). Deve quindi chiamare [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) con il valore dell' [**\_ ambito di \_ gestione \_ del profilo WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) appropriato per ottenere il nuovo profilo colore attivo per il monitoraggio. Si noti che non tutte le modifiche apportate alla chiave del registro di sistema corrispondono a una modifica effettiva nel profilo colori attualmente attivo; l'app deve controllare se il profilo restituito da **WcsGetDefaultColorProfile** è stato effettivamente modificato.

### <a name="universal-windows-uwp-apps"></a>App di Windows universale (UWP)

Le app di Windows universale non hanno accesso alle chiavi del registro di sistema indicate sopra. Devono invece registrare un gestore per l'evento [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) . Questo evento viene generato ogni volta che viene modificato il profilo colori attivo per il monitoraggio in cui è in esecuzione l'applicazione. ColorProfileChanged prende in considerazione la possibilità di usare associazioni di profili per singolo utente o a livello di sistema; Queste informazioni sono astratte dalle app UWP.

Quando si risponde all'evento ColorProfileChanged, l'app deve eseguire una query sul profilo attualmente attivo usando [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).

 

 