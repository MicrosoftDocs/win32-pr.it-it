---
description: Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160, 4.0 e versioni precedenti.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Non supportato in Windows Installer 4,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4307422c71976057948759078dc321e38dc543b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321104"
---
# <a name="not-supported-in-windows-installer-40"></a>Non supportato in Windows Installer 4,0

Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer 4,0 e versioni precedenti. L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata. Vedere la documentazione principale per determinare quale versione di Windows Installer è necessaria per una determinata funzionalità. Per informazioni sulle altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,0 è disponibile per Microsoft Windows Server 2008 e Windows Vista. Per un elenco completo di tutte le versioni di Windows Installer e dei ridistribuibili, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

Le funzionalità seguenti non sono supportate in Windows Installer 4,0 e versioni precedenti.

[Funzioni di installazione](installer-functions.md)

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
-   [Tabella componenti](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) Colonna ExtendedType  
    

[Opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[Criteri di sistema](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

Prototipi di funzioni di callback

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[Analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) verifica che nessun componente includa entrambi gli attributi **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .

## <a name="notes"></a>Note

Windows Installer 4,0 non è possibile eseguire [più installazioni di pacchetti](multiple-package-installations.md) utilizzando l' [*elaborazione delle transazioni*](t-gly.md).

Con Windows Installer 4,0 o versioni precedenti del programma di installazione, gli aggiornamenti piccoli e quelli secondari possono avere esito negativo quando si usa il criterio [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) o la proprietà [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) perché l'aggiornamento rimuove un componente.

Un'interfaccia utente personalizzata non può essere incorporata all'interno del pacchetto di Windows Installer usando il metodo descritto in uso di un'interfaccia utente [incorporata](using-an-embedded-ui.md).

 

 



