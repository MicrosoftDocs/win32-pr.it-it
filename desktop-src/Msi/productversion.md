---
description: Il valore della proprietà ProductVersion è la versione del prodotto in formato stringa.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Proprietà ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330381"
---
# <a name="productversion-property"></a>Proprietà ProductVersion

Il valore della proprietà **ProductVersion** è la versione del prodotto in formato stringa. Questa proprietà è obbligatoria.

Il formato della stringa è il seguente:

<dl> principale.secondario.build  
</dl>

Il primo campo è la versione principale e ha un valore massimo di 255. Il secondo campo è la versione secondaria e ha un valore massimo di 255. Il terzo campo è denominato versione build o versione di aggiornamento e ha un valore massimo di 65.535.

## <a name="remarks"></a>Commenti

Almeno uno dei tre campi di **ProductVersion** deve cambiare per un aggiornamento mediante la tabella di [aggiornamento](upgrade-table.md). Qualsiasi aggiornamento che modifica solo il codice del pacchetto, ma lascia invariato **ProductVersion** e [**ProductCode**](productcode.md) è chiamato un [piccolo aggiornamento](small-updates.md). I campi di tre versioni vengono forniti principalmente per praticità. Se, ad esempio, si desidera modificare **ProductVersion**, ma non si desidera modificare le versioni principale o secondaria, è possibile modificare la versione di compilazione.

Si noti che Windows Installer utilizza solo i primi tre campi della versione del prodotto. Se si include un quarto campo nella versione del prodotto, il programma di installazione ignorerà il quarto campo.

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

[aggiornamento ridotto](small-updates.md)
</dt> </dl>

 

 




