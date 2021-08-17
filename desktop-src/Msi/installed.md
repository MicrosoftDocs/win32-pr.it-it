---
description: La proprietà Installed viene impostata solo se il prodotto è installato per computer o per l'utente corrente.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Proprietà Installed
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5925f68595f6b0975e64281be0ba7326fa831d08f0298f9b84375df97e5196c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633524"
---
# <a name="installed-property"></a>Proprietà Installed

La **proprietà Installed** viene impostata solo se il prodotto è installato per computer o per l'utente corrente. Questa proprietà non viene impostata se il prodotto è installato per un utente diverso.

La **proprietà Installed** può essere usata nelle espressioni condizionali per determinare se un prodotto è installato per computer o per l'utente corrente. Ad esempio, la proprietà può essere utilizzata nella colonna condizionale di una tabella di sequenza o per distinguere tra una prima installazione e un'installazione di manutenzione.

Per determinare se il prodotto è installato per un utente diverso, controllare la [**proprietà ProductState.**](productstate.md)

Il valore della [**proprietà ProductVersion**](productversion.md) è la versione del prodotto in formato stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




