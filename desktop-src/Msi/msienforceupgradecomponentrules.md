---
description: Impostare la proprietà MSIENFORCEUPGRADECOMPONENTRULES su 1 nella riga di comando o nella tabella Proprietà per applicare le regole del componente di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: MsiENFORCEUPGRADECOMPONENTRULES - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11535beb45ac521e59ec31c5e5231b23549394b75e5df2372ba4295471ea8008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945045"
---
# <a name="msienforceupgradecomponentrules-property"></a>MsiENFORCEUPGRADECOMPONENTRULES - proprietà

Impostare la **proprietà MSIENFORCEUPGRADECOMPONENTRULES** su 1 nella riga di comando o [](small-updates.md) nella tabella [](minor-upgrades.md) [Proprietà](property-table.md) per applicare le regole del componente di aggiornamento durante piccoli aggiornamenti e aggiornamenti secondari di un determinato prodotto. Per applicare le regole durante piccoli aggiornamenti e aggiornamenti secondari di tutti i prodotti nel computer, impostare il criterio [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) su 1.

Quando la proprietà o i criteri sono [](minor-upgrades.md) impostati su 1, [](small-updates.md) gli aggiornamenti di piccole dimensioni e gli aggiornamenti secondari possono non riuscire perché l'aggiornamento tenta di eseguire le operazioni seguenti che violano le regole del componente di aggiornamento:

-   Aggiungere una nuova funzionalità nella parte superiore o centrale di un albero delle caratteristiche esistente.

    La nuova funzionalità deve essere aggiunta come nuova funzionalità foglia a un albero delle funzionalità esistente.

    In questo caso, il [**Codice Prodotto**](productcode.md) del prodotto può essere modificato e l'aggiornamento può essere considerato come [un aggiornamento principale.](major-upgrades.md)

-   Rimuovere un componente da una funzionalità.

    Ciò può verificarsi anche se si modifica il GUID di un componente. Il componente identificato dal GUID originale sembra essere rimosso e il componente identificato dal nuovo GUID viene visualizzato come nuovo componente.

    **Windows Installer 4.5 e versioni successive:** Il componente può essere rimosso correttamente usando Windows Installer 4.5 e versioni successive impostando l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella tabella dei componenti o impostando la [**proprietà MSIUNINSTALLSUPERSEDCOMPONENTS.**](msiuninstallsupersededcomponents.md) [](component-table.md)

    In alternativa, il [**ProductCode**](productcode.md) del prodotto può essere modificato e l'aggiornamento può essere considerato come [un aggiornamento principale.](major-upgrades.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




