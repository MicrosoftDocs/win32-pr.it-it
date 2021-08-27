---
description: Il valore della proprietà ProductVersion è la versione del prodotto in formato stringa.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09d2fb436dffba5ae2fa98144d39e5824d09796472297db116a2a4543d55168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074641"
---
# <a name="productversion-property"></a>ProductVersion - proprietà

Il valore della **proprietà ProductVersion** è la versione del prodotto in formato stringa. Questa proprietà è REQUIRED.

Il formato della stringa è il seguente:

<dl> principale.secondario.build  
</dl>

Il primo campo è la versione principale e ha un valore massimo di 255. Il secondo campo è la versione secondaria e ha un valore massimo di 255. Il terzo campo è denominato versione della build o versione di aggiornamento e ha un valore massimo di 65.535.

## <a name="remarks"></a>Commenti

Almeno uno dei tre campi di **ProductVersion** deve essere modificato per un aggiornamento usando la [tabella Upgrade](upgrade-table.md). Qualsiasi aggiornamento che modifica solo il codice del pacchetto, ma lascia **invariati ProductVersion** e [**ProductCode**](productcode.md) viene chiamato [aggiornamento di piccole dimensioni.](small-updates.md) I campi delle tre versioni vengono forniti principalmente per praticità. Ad esempio, se si vuole modificare **ProductVersion**, ma non la versione principale o secondaria, è possibile modificare la versione della build.

Si noti Windows Installer usa solo i primi tre campi della versione del prodotto. Se si include un quarto campo nella versione del prodotto, il programma di installazione ignora il quarto campo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Applicazione di patch e aggiornamenti](patching-and-upgrades.md)
</dt> <dt>

[aggiornamento di piccole dimensioni](small-updates.md)
</dt> </dl>

 

 




