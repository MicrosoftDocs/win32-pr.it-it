---
Description: La proprietà ALLUSERS configura il contesto di installazione del pacchetto.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: AllUSERS - proprietà
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: b6412707d6ef46b55d1f8add3de56a24e6f970dc9fa7f0353dce6ec9efa9f531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581881"
---
# <a name="allusers-property"></a>AllUSERS - proprietà

La **proprietà ALLUSERS** configura il contesto di installazione del pacchetto. Il programma di installazione di Windows esegue un'installazione per utente o per computer a seconda dei privilegi di accesso dell'utente, se sono necessari privilegi elevati per installare l'applicazione, il valore della proprietà **ALLUSERS,** il valore della [**proprietà MSIINSTALLPERUSER**](msiinstallperuser.md) e la versione del sistema operativo.

Il valore della proprietà **ALLUSERS,** in fase di installazione, determina il [contesto di installazione.](installation-context.md)

-   Il valore della proprietà **ALLUSERS** pari a 1 specifica il contesto di installazione per computer.
-   Il **valore della proprietà ALLUSERS** di una stringa vuota ("") specifica il contesto di installazione per utente.
-   Se il valore della proprietà **ALLUSERS** è impostato su 2, il programma di installazione di Windows reimposta sempre il valore della proprietà **ALLUSERS** su 1 ed esegue un'installazione per computer oppure reimposta il valore della proprietà **ALLUSERS** su una stringa vuota ("") ed esegue un'installazione per utente. Il valore ALLUSERS=2 consente al sistema di reimpostare il valore di **ALLUSERS** e il contesto di installazione, in base ai privilegi dell'utente e alla versione di Windows.

    **Windows 7:** Impostare la **proprietà ALLUSERS** su 2 per usare la [**proprietà MSIINSTALLPERUSER**](msiinstallperuser.md) per specificare il contesto di installazione. Impostare la **proprietà MSIINSTALLPERUSER** su una stringa vuota ("") per un'installazione per computer. Impostare la **proprietà MSIINSTALLPERUSER** su 1 per un'installazione per utente. Se il pacchetto è stato scritto seguendo le linee guida di sviluppo descritte in [Creazione](single-package-authoring.md)di pacchetti singoli, gli utenti che hanno accesso utente possono installare nel contesto per utente senza dover fornire credenziali di controllo dell'account utente. Se l'utente dispone di privilegi di accesso utente, il programma di installazione esegue un'installazione per computer solo se nella finestra di dialogo Controllo dell'account utente vengono fornite credenziali di amministratore.

    **Windows Vista:** Impostare la **proprietà ALLUSERS** su 2 e Windows installer è conforme al [*controllo dell'account*](u-gly.md) utente. Se l'utente dispone di privilegi di accesso utente e ALLUSERS=2, il programma di installazione esegue un'installazione per computer solo se vengono fornite credenziali di amministratore alla finestra di dialogo controllo dell'account utente. Se il controllo dell'account utente è abilitato e non vengono fornite le credenziali di amministratore corrette, l'installazione non riesce e viene visualizzato un errore che indica che sono necessari privilegi di amministratore. Se il controllo dell'account utente è disabilitato dalla chiave del Registro di sistema, dai criteri di gruppo o dal Pannello di controllo, la finestra di dialogo Controllo dell'account utente non viene visualizzata e l'installazione non riesce e viene visualizzato un errore che indica che sono necessari privilegi di amministratore.

    **Windows XP:** Impostare la **proprietà ALLUSERS** su 2 e Windows installer esegue un'installazione per utente se l'utente dispone di privilegi di accesso utente.

-   Se il valore della **proprietà ALLUSERS** non è uguale a 2, il Windows Installer ignora il valore della [**proprietà MSIINSTALLPERUSER.**](msiinstallperuser.md)

## <a name="example"></a>Esempio

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) in GitHub.

## <a name="default-value"></a>Valore predefinito

Il contesto di installazione predefinito consigliato è per utente. Se **ALLUSERS non** è impostato, il programma di installazione esegue un'installazione per utente. È possibile assicurarsi che **la proprietà ALLUSERS** non sia stata impostata impostandone il valore su una stringa vuota (""), ALLUSERS="".

## <a name="remarks"></a>Commenti

Il [](installation-context.md) contesto di installazione determina i valori delle proprietà [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder.**](commonfiles64folder.md) Il contesto di installazione determina le parti [](registry-table.md) del Registro di sistema in cui vengono scritte o rimosse le voci nella tabella Registro di sistema e nella tabella [RemoveRegistry](removeregistry-table.md), con -1 nella colonna Radice .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



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

 

 




