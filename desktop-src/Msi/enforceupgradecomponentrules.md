---
description: Si tratta di un criterio di sistema per computer che può essere usato per applicare le regole dei componenti di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967683"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Si tratta di un criterio di [sistema](system-policy.md) per computer che può essere usato per applicare le regole dei componenti di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md).

Impostare il criterio EnforceUpgradeComponentRules su 1 per applicare le regole del componente di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md) di tutti i prodotti nel computer. Per applicare le regole durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto, impostare la proprietà [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) su 1 nella riga di comando o nella [tabella delle proprietà](property-table.md).

Quando la proprietà o il criterio è stato impostato su 1, [gli aggiornamenti piccoli](small-updates.md) e quelli [secondari](minor-upgrades.md) possono avere esito negativo perché l'aggiornamento tenta di eseguire le operazioni seguenti:

-   Consente di aggiungere una nuova funzionalità alla parte superiore o centrale di un albero delle funzionalità esistente.

    La nuova funzionalità deve essere aggiunta come nuova funzionalità foglia a un albero delle funzionalità esistente.

    In questo caso, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e gli aggiornamenti possono essere considerati come un [aggiornamento importante](major-upgrades.md).

-   Rimuovere un componente da una funzionalità.

    Questa situazione può verificarsi anche se si modifica il GUID di un componente. Il componente identificato dal GUID originale sembra essere rimosso e il componente identificato dal nuovo GUID viene visualizzato come nuovo componente.

    **Windows Installer 4,5 e versioni successive:** Il componente può essere rimosso correttamente usando Windows Installer 4,5 o versione successiva impostando l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md) o impostando la proprietà [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    In alternativa, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e gli aggiornamenti possono essere considerati come un [aggiornamento importante](major-upgrades.md).

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



