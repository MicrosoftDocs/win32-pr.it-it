---
description: Le proprietà MSIINSTALLPERUSER e ALLUSERS possono essere impostate dall'utente al momento dell'installazione, tramite l'interfaccia utente o la riga di comando, per richiedere che l'Windows Installer installare un pacchetto a doppio scopo per l'utente corrente o per tutti gli utenti del computer.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Proprietà MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325464"
---
# <a name="msiinstallperuser-property"></a>Proprietà MSIINSTALLPERUSER

Le proprietà **MSIINSTALLPERUSER** e [**ALLUSERS**](allusers.md) possono essere impostate dall'utente al momento dell'installazione, tramite l'interfaccia utente o la riga di comando, per richiedere che l'Windows Installer installare un pacchetto a doppio scopo per l'utente corrente o per tutti gli utenti del computer. Per usare la proprietà **MSIINSTALLPERUSER** , il valore della proprietà [**ALLUSERS**](allusers.md) deve essere 2 e il pacchetto deve essere stato creato per essere in grado di eseguire l'installazione in un contesto per utente o per computer. Per informazioni sulla creazione di un pacchetto a doppio scopo, vedere [creazione di pacchetti singoli](single-package-authoring.md). Se il valore della proprietà **ALLUSERS** non è uguale a 2, il valore della proprietà **MSIINSTALLPERUSER** viene ignorato e non ha alcun effetto sull'installazione. Il valore della proprietà **MSIINSTALLPERUSER** viene ignorato quando si installa il pacchetto utilizzando Windows Installer 4,5 o versioni precedenti.

Per richiedere che l'Windows Installer installi il pacchetto a doppio scopo nel contesto di [installazione](installation-context.md)per computer, l'utente può impostare il valore della proprietà **MSIINSTALLPERUSER** su una stringa vuota ("") e il valore della proprietà [**ALLUSERS**](allusers.md) su 2 usando un'interfaccia utente creata o una riga di comando.

Per richiedere che l'Windows Installer installi il pacchetto a doppio scopo nel contesto di [installazione](installation-context.md)per utente, l'utente può impostare il valore della proprietà **MSIINSTALLPERUSER** su 1 e il valore della proprietà [**ALLUSERS**](allusers.md) su 2 usando un'interfaccia utente creata o una riga di comando.

Se il valore della proprietà [**ALLUSERS**](allusers.md) non è uguale a 2, il Windows Installer ignora il valore della proprietà **MSIINSTALLPERUSER** . Se Windows Installer installa l'applicazione nel contesto per computer, reimposta il valore della proprietà **ALLUSERS** su 1. Se Windows Installer installa l'applicazione nel contesto per utente, reimposta il valore della proprietà **ALLUSERS** su una stringa vuota (""). Le applicazioni installate per utente ricevono quindi tutti gli aggiornamenti o le riparazioni per ogni utente e le applicazioni installate per computer ricevono aggiornamenti o riparazioni per computer.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** la proprietà **MSIINSTALLPERUSER** viene ignorata dalle versioni precedenti a Windows Installer 5,0.

## <a name="default-value"></a>Valore predefinito

Il contesto di installazione predefinito consigliato è per utente per un pacchetto a doppio scopo. Creare MSIINSTALLPERUSER = 1 e ALLUSERS = 2 nella [tabella delle proprietà](property-table.md) del pacchetto a doppio scopo per specificare per utente come contesto di installazione predefinito.

## <a name="remarks"></a>Commenti

È possibile verificare che la proprietà **MSIINSTALLPERUSER** non sia stata impostata impostando il relativo valore su una stringa vuota (""), MSIINSTALLPERUSER = "".

Il contesto di installazione determina i valori delle proprietà [**includevano**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**dei**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**cartellamodelli**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)e [**CommonFiles64Folder**](commonfiles64folder.md) . Il contesto di installazione determina le parti del registro di sistema in cui vengono scritte o rimosse le voci della tabella [del registro di sistema](registry-table.md) e della [tabella RemoveRegistry](removeregistry-table.md), con-1 nella colonna radice. Per informazioni sul contesto di installazione, vedere [contesto di installazione](installation-context.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[Contesto di installazione](installation-context.md)
</dt> <dt>

[Creazione di pacchetti singoli](single-package-authoring.md)
</dt> </dl>

 

 




