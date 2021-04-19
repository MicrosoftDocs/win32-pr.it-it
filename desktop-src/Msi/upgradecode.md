---
description: La proprietà UpgradeCode è un GUID che rappresenta un set correlato di prodotti. UpgradeCode viene utilizzato nella tabella di aggiornamento per cercare le versioni correlate del prodotto già installato. Questa proprietà viene utilizzata dall'azione RegisterProduct.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Proprietà UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328147"
---
# <a name="upgradecode-property"></a>Proprietà UpgradeCode

La proprietà **UpgradeCode** è un GUID che rappresenta un set correlato di prodotti. **UpgradeCode** viene utilizzato nella tabella di [aggiornamento](upgrade-table.md) per cercare le versioni correlate del prodotto già installato.

Questa proprietà viene utilizzata dall' [azione RegisterProduct](registerproduct-action.md).

## <a name="remarks"></a>Commenti

Si consiglia vivamente agli autori dei pacchetti di installazione di specificare un **UpgradeCode** per la propria applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
</dt> <dt>

[Preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




