---
Description: La proprietà ALLUSERS configura il contesto di installazione del pacchetto.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: Proprietà ALLUSERS
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331617"
---
# <a name="allusers-property"></a>Proprietà ALLUSERS

La proprietà **ALLUSERS** configura il contesto di installazione del pacchetto. Il Windows Installer esegue un'installazione per utente o per computer a seconda dei privilegi di accesso dell'utente, se sono necessari privilegi elevati per installare l'applicazione, il valore della proprietà **ALLUSERS** , il valore della proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) e la versione del sistema operativo.

Il valore della proprietà **ALLUSERS** , al momento dell'installazione, determina il [contesto di installazione](installation-context.md).

-   Il valore 1 della proprietà **ALLUSERS** specifica il contesto di installazione per computer.
-   Il valore della proprietà **ALLUSERS** di una stringa vuota ("") specifica il contesto di installazione per utente.
-   Se il valore della proprietà **ALLUSERS** è impostato su 2, il Windows Installer Reimposta sempre il valore della proprietà **ALLUSERS** su 1 ed esegue un'installazione per computer oppure reimposta il valore della proprietà **ALLUSERS** su una stringa vuota ("") ed esegue un'installazione per utente. Il valore ALLUSERS = 2 consente al sistema di reimpostare il valore di **ALLUSERS** e il contesto di installazione, a seconda dei privilegi dell'utente e della versione di Windows.

    **Windows 7:** Impostare la proprietà **ALLUSERS** su 2 per utilizzare la proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) per specificare il contesto di installazione. Impostare la proprietà **MSIINSTALLPERUSER** su una stringa vuota ("") per un'installazione per computer. Impostare la proprietà **MSIINSTALLPERUSER** su 1 per l'installazione per utente. Se il pacchetto è stato scritto seguendo le linee guida per lo sviluppo descritte in [creazione di pacchetti singoli](single-package-authoring.md), gli utenti che dispongono dell'accesso utente possono installare nel contesto per utente senza dover fornire le credenziali di UAC. Se l'utente dispone dei privilegi di accesso utente, il programma di installazione esegue un'installazione per computer solo se vengono fornite le credenziali di amministratore alla finestra di dialogo controllo dell'account utente.

    **Windows Vista:** Impostare la proprietà **ALLUSERS** su 2 e Windows Installer conforme a [*controllo dell'account utente*](u-gly.md) (UAC). Se l'utente dispone dei privilegi di accesso utente e ALLUSERS = 2, il programma di installazione esegue un'installazione per computer solo se vengono fornite le credenziali di amministratore alla finestra di dialogo controllo dell'account utente. Se UAC è abilitato e non vengono fornite le credenziali di amministratore corrette, l'installazione non riesce e viene visualizzato un errore che informa che sono necessari privilegi di amministratore. Se UAC è disabilitato dalla chiave del registro di sistema, da criteri di gruppo o dal pannello di controllo, la finestra di dialogo controllo dell'account utente non viene visualizzata e l'installazione ha esito negativo con un errore che informa che sono necessari privilegi di amministratore.

    **Windows XP:** Impostare la proprietà **ALLUSERS** su 2 e Windows Installer esegue un'installazione per utente se l'utente dispone dei privilegi di accesso utente.

-   Se il valore della proprietà **ALLUSERS** non è uguale a 2, il Windows Installer ignora il valore della proprietà [**MSIINSTALLPERUSER**](msiinstallperuser.md) .

## <a name="example"></a>Esempio

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) in GitHub.

## <a name="default-value"></a>Valore predefinito

Il contesto di installazione predefinito consigliato è per singolo utente. Se **ALLUSERS** non è impostato, il programma di installazione esegue un'installazione per utente. È possibile verificare che la proprietà **ALLUSERS** non sia stata impostata impostando il relativo valore su una stringa vuota (""), ALLUSERS = "".

## <a name="remarks"></a>Commenti

Il [contesto di installazione](installation-context.md) determina i valori delle proprietà [**includevano**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**dei**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**cartellamodelli**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) . Il contesto di installazione determina le parti del registro di sistema in cui vengono scritte o rimosse le voci della tabella [del registro di sistema](registry-table.md) e della [tabella RemoveRegistry](removeregistry-table.md), con-1 nella colonna radice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[Contesto di installazione](installation-context.md)
</dt> <dt>

[Creazione di pacchetti singoli](single-package-authoring.md)
</dt> </dl>

 

 




