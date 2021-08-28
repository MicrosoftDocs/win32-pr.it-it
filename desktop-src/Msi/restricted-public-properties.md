---
description: In alcuni casi, un utente che non è un amministratore di sistema può eseguire l'override solo di un elenco approvato di proprietà pubbliche Windows programma di installazione.
ms.assetid: e16e8187-75b6-4104-a53c-928a56fcee6b
title: Proprietà pubbliche con restrizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af09200f10261e50564ae79dbad961474d23d8a6354cee7344aa107c8b73fb57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979301"
---
# <a name="restricted-public-properties"></a>Proprietà pubbliche con restrizioni

Nel caso di un'installazione gestita, l'autore [](public-properties.md) del pacchetto potrebbe dover limitare le proprietà pubbliche che vengono passate al lato server e possono essere modificate da un utente che non è un amministratore di sistema. Alcune restrizioni sono in genere necessarie per mantenere un ambiente sicuro quando l'installazione richiede che il programma di installazione usi privilegi elevati. Se vengono soddisfatte tutte le condizioni seguenti, un utente che non è un amministratore di sistema può eseguire l'override solo di un elenco approvato di proprietà pubbliche con restrizioni:

-   Il sistema è Windows 2000.
-   L'utente non è un amministratore di sistema.
-   L'applicazione o il prodotto viene installato con privilegi elevati.

Se tutte le condizioni precedenti sono vere, il programma di installazione utilizza per impostazione predefinita l'elenco seguente di proprietà pubbliche con restrizioni che possono essere modificate da qualsiasi utente:

-   [**Azione**](action.md)
-   [**AFTERREBOOT**](afterreboot.md)
-   [**Allusers**](allusers.md)
-   [**EXECUTEACTION**](executeaction.md)
-   [**EXECUTEMODE**](executemode.md)
-   [**FILEADDDEFAULT**](fileadddefault.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**INSTALLLEVEL**](installlevel.md)
-   [**LIMITUI**](limitui.md)
-   [**LOGACTION**](logaction.md)
-   [**NOCOMPANYNAME**](nocompanyname.md)
-   [**NOUSERNAME**](nousername.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**benda**](patch.md)
-   [**PRIMARYFOLDER**](primaryfolder.md)
-   [**PROMPTROLLBACKCOST**](promptrollbackcost.md)
-   [**Riavviare**](reboot.md)
-   [**REINSTALL**](reinstall.md)
-   [**REINSTALLMODE**](reinstallmode.md)
-   [**riassumere**](resume.md)
-   [**SEQUENCE**](sequence.md)
-   [**SHORTFILENAMES**](shortfilenames.md)
-   [**Trasforma**](transforms.md)
-   [**TRANSFORMSATSOURCE**](transformsatsource.md)

L'autore di un pacchetto di installazione può estendere questo elenco predefinito per includere proprietà pubbliche aggiuntive usando la [**proprietà SecureCustomProperties.**](securecustomproperties.md)

[**L'impostazione della proprietà EnableUserControl**](-enableusercontrol.md) o dei [criteri di sistema EnableUserControl](enableusercontrol.md)[estende](system-policy.md) l'elenco a tutte le proprietà pubbliche. Tutti gli utenti possono quindi modificare qualsiasi proprietà pubblica.

Il programma di installazione [**imposta la proprietà RestrictedUserControl**](restrictedusercontrol.md) ogni volta che l'elenco di proprietà pubbliche passate al server da utenti non amministratori è limitato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> </dl>

 

 



