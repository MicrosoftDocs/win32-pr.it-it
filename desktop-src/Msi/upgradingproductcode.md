---
description: La proprietà UPGRADINGPRODUCTCODE viene impostata dal programma Windows quando un aggiornamento rimuove un'applicazione.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: UPGRADINGPRODUCTCODE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f5b0096878d06c4eb3880ab8d965265b04114bcf4e3d732d8243bb4fb02cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809511"
---
# <a name="upgradingproductcode-property"></a>UPGRADINGPRODUCTCODE - proprietà

La **proprietà UPGRADINGPRODUCTCODE viene** impostata dal programma Windows quando un aggiornamento rimuove un'applicazione. Il programma di installazione imposta questa proprietà quando esegue [l'azione RemoveExistingProducts](removeexistingproducts-action.md). Questa proprietà non viene impostata rimuovendo un'applicazione tramite Installazione applicazioni in Pannello di controllo. Un'applicazione determina se viene rimossa da un aggiornamento o da Installazione applicazioni controllando **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




