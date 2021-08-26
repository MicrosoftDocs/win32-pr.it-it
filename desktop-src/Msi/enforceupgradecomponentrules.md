---
description: Si tratta di criteri di sistema per computer che possono essere usati per applicare regole del componente di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882d7df0e794dfb89ab2211db1fada576bd6e056972810d582385c1404e625a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086071"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Si tratta di un criterio di [sistema](system-policy.md) per computer che può essere usato per applicare regole del componente di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari.](minor-upgrades.md)

Impostare il criterio EnforceUpgradeComponentRules su 1 [](small-updates.md) per applicare [](minor-upgrades.md) le regole del componente di aggiornamento durante gli aggiornamenti di piccole dimensioni e gli aggiornamenti secondari di tutti i prodotti nel computer. Per applicare le regole durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto, impostare la proprietà [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) su 1 nella riga di comando o nella tabella [Delle proprietà](property-table.md).

Quando la proprietà o il criterio è stato [](minor-upgrades.md) impostato su 1, [](small-updates.md) gli aggiornamenti di piccole dimensioni e gli aggiornamenti secondari possono non riuscire perché l'aggiornamento tenta di eseguire le operazioni seguenti:

-   Aggiungere una nuova funzionalità nella parte superiore o centrale di un albero delle caratteristiche esistente.

    La nuova funzionalità deve essere aggiunta come nuova funzionalità foglia a un albero delle funzionalità esistente.

    In questo caso, [**il Codice Prodotto**](productcode.md) del prodotto può essere modificato e gli aggiornamenti possono essere considerati come un aggiornamento [principale.](major-upgrades.md)

-   Rimuovere un componente da una funzionalità.

    Ciò può verificarsi anche se si modifica il GUID di un componente. Il componente identificato dal GUID originale sembra essere rimosso e il componente identificato dal nuovo GUID viene visualizzato come nuovo componente.

    **Windows Installer 4.5 e versioni successive:** Il componente può essere rimosso correttamente usando Windows Installer 4.5 o versione successiva impostando l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella tabella [Component](component-table.md) o impostando la [**proprietà MSIUNINSTALLSUPERSEDCOMPONENTS.**](msiuninstallsupersededcomponents.md)

    In alternativa, il [**ProductCode**](productcode.md) del prodotto può essere modificato e gli aggiornamenti possono essere considerati come [un aggiornamento principale.](major-upgrades.md)

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del computer** \\  \\ **locale** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



