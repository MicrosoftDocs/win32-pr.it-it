---
description: La proprietà UPGRADINGPRODUCTCODE viene impostata da Windows Installer quando un aggiornamento rimuove un'applicazione.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Proprietà UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328136"
---
# <a name="upgradingproductcode-property"></a>Proprietà UPGRADINGPRODUCTCODE

La proprietà **UPGRADINGPRODUCTCODE** viene impostata da Windows Installer quando un aggiornamento rimuove un'applicazione. Il programma di installazione imposta questa proprietà quando esegue l' [azione RemoveExistingProducts](removeexistingproducts-action.md). Questa proprietà non viene impostata rimuovendo un'applicazione utilizzando Installazione applicazioni nel pannello di controllo. Un'applicazione determina se viene rimossa da un aggiornamento o da installazione applicazioni controllando **UPGRADINGPRODUCTCODE**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




