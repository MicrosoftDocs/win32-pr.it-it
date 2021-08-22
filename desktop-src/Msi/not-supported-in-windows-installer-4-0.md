---
description: Le funzioni, le tabelle e le proprietà del programma di installazione di Windows elencate in questa pagina non sono supportate da Windows Installer&\# 160;4.0 e versioni precedenti.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Non supportato in Windows Installer 4.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558801"
---
# <a name="not-supported-in-windows-installer-40"></a>Non supportato in Windows Installer 4.0

Le Windows installer, le tabelle e le proprietà elencate in questa pagina non sono supportate da Windows Installer 4.0 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale versione Windows installer è necessaria per una particolare funzionalità. Per informazioni su altre versioni Windows Installer, vedere Novità del programma [di Windows Installer.](what-s-new-in-windows-installer.md)

Windows Il programma di installazione 4.0 è disponibile per Microsoft Windows Server 2008 e Windows Vista. Per un elenco completo di tutte le Windows e ridistribuibili del programma di installazione, vedere Versioni rilasciate di [Windows Installer.](released-versions-of-windows-installer.md)

Le funzionalità seguenti non sono supportate in Windows Installer 4.0 e versioni precedenti.

[Funzioni del programma di installazione](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Proprietà](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[Tabelle di database](database-tables.md)

-   [Tabella MsiEmbeddedChainer](msiembeddedchainer-table.md)
-   [Tabella MsiEmbeddedUI](msiembeddedui-table.md)
-   [Tabella MsiPackageCertificate](msipackagecertificate-table.md)
-   [Tabella dei componenti](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) Colonna ExtendedType  
    

[Opzione di disinstallazione della patch azione personalizzata](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[Criteri di sistema](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

Prototipi di funzioni di callback

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[Analizzatori di coerenza interna - ICE](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) verifica che nessun componente abbia entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence.**

## <a name="notes"></a>Note

Windows Il programma di installazione 4.0 non è in [grado di eseguire più installazioni di pacchetti](multiple-package-installations.md) utilizzando [*l'elaborazione delle transazioni*](t-gly.md).

Usando Windows Installer 4.0 o versioni precedenti del programma di installazione, è possibile che piccoli aggiornamenti e aggiornamenti secondari non riescano quando si usa il criterio [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) o la proprietà [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) perché l'aggiornamento rimuove un componente.

Non è possibile incorporare un'interfaccia utente personalizzata all'interno del Windows Installer usando il metodo descritto in [Uso di un'interfaccia utente incorporata.](using-an-embedded-ui.md)

 

 



