---
description: In alcuni casi, un utente che non è un amministratore di sistema può solo ignorare un elenco approvato di proprietà pubbliche con restrizioni Windows Installer.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Proprietà pubbliche limitate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f08be7f625cd45cdb48373eb0107ade708949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315893"
---
# <a name="restricted-public-properties"></a>Proprietà pubbliche limitate

Nel caso di un'installazione gestita, l'autore del pacchetto potrebbe dover limitare le [proprietà pubbliche](public-properties.md) che vengono passate al lato server e possono essere modificate da un utente che non è un amministratore di sistema. Alcune restrizioni sono in genere necessarie per mantenere un ambiente protetto quando l'installazione richiede che il programma di installazione utilizzi privilegi elevati. Se vengono soddisfatte tutte le condizioni seguenti, un utente che non è un amministratore di sistema può solo eseguire l'override di un elenco approvato di proprietà pubbliche limitate:

-   Il sistema è Windows 2000.
-   L'utente non è un amministratore di sistema.
-   È in corso l'installazione dell'applicazione o del prodotto con privilegi elevati.

Se tutte le condizioni precedenti sono vere, il programma di installazione viene impostato sul seguente elenco di proprietà pubbliche con restrizioni che possono essere modificate da qualsiasi utente:

-   [**AZIONE**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**ALLUSERS**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**EXECUTEMODE**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**NoCompanyName**](nocompanyname.md)
-   [**NOUSERNAME**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**PATCH**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**RIAVVIO**](reboot.md)
-   [**REINSTALL**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**RIPRENDERE**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**TRASFORMA**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

L'autore di un pacchetto di installazione può estendere questo elenco predefinito per includere proprietà pubbliche aggiuntive tramite la proprietà [**SecureCustomProperties**](securecustomproperties.md) .

Se si imposta la proprietà [**EnableUserControl**](-enableusercontrol.md) o il [criterio di sistema](system-policy.md) [EnableUserControl](enableusercontrol.md), l'elenco viene esteso a tutte le proprietà pubbliche. Tutti gli utenti possono quindi modificare qualsiasi proprietà pubblica.

Il programma di installazione imposta la proprietà [**RestrictedUserControl**](restrictedusercontrol.md) ogni volta che l'elenco di proprietà pubbliche passato al server da utenti non amministratori è limitato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> </dl>

 

 



