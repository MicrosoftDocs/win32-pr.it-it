---
description: Impostare la proprietà MSIENFORCEUPGRADECOMPONENTRULES su 1 nella riga di comando o nella tabella delle proprietà per applicare le regole del componente di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Proprietà MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329123"
---
# <a name="msienforceupgradecomponentrules-property"></a>Proprietà MSIENFORCEUPGRADECOMPONENTRULES

Impostare la proprietà **MSIENFORCEUPGRADECOMPONENTRULES** su 1 nella riga di comando o nella [tabella delle proprietà](property-table.md) per applicare le regole del componente di aggiornamento durante [piccoli aggiornamenti](small-updates.md) e [aggiornamenti secondari](minor-upgrades.md) di un determinato prodotto. Per applicare le regole durante piccoli aggiornamenti e aggiornamenti secondari di tutti i prodotti nel computer, impostare il criterio [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) su 1.

Quando la proprietà o il criterio è impostato su 1, [gli aggiornamenti piccoli](small-updates.md) e [secondari](minor-upgrades.md) possono avere esito negativo perché l'aggiornamento tenta di eseguire le operazioni seguenti che violano le regole del componente di aggiornamento:

-   Consente di aggiungere una nuova funzionalità alla parte superiore o centrale di un albero delle funzionalità esistente.

    La nuova funzionalità deve essere aggiunta come nuova funzionalità foglia a un albero delle funzionalità esistente.

    In questo caso, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e l'aggiornamento può essere considerato un [aggiornamento importante](major-upgrades.md).

-   Rimuovere un componente da una funzionalità.

    Questa situazione può verificarsi anche se si modifica il GUID di un componente. Il componente identificato dal GUID originale sembra essere rimosso e il componente identificato dal nuovo GUID viene visualizzato come nuovo componente.

    **Windows Installer 4,5 e versioni successive:** Il componente può essere rimosso correttamente usando Windows Installer 4,5 e versioni successive impostando l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md) o impostando la proprietà [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    In alternativa, è possibile modificare il [**ProductCode**](productcode.md) del prodotto e l'aggiornamento può essere considerato un [aggiornamento importante](major-upgrades.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




