---
description: Impostare la proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS su 1 nella tabella Proprietà o in una riga di comando.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: MSIUNINSTALLSUPERSEDEDCOMPONENTS - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae30e142167e2d080fa4c74c046625338fbf92fd4476b0339d60f77e321ab54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943942"
---
# <a name="msiuninstallsupersededcomponents-property"></a>MSIUNINSTALLSUPERSEDEDCOMPONENTS - proprietà

Impostare la **proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS** su 1 nella tabella [Proprietà](property-table.md) o in una riga di comando. Quando questa proprietà è stata impostata su 1, il programma di installazione determina se i componenti nelle patch sostituite stanno diventando ridondanti. Il programma di installazione può annullare la registrazione e disinstallare i componenti ridondanti per evitare di lasciare componenti orfani nel computer.

L'impostazione di questa proprietà influisce sui componenti di tutte le patch sostituite. Per abilitare questa funzionalità per i singoli componenti, usare l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md).

**[Windows Installer 4.0 e versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. Le versioni precedenti Windows Installer 4.5 ignorano la **proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.5 o Windows Installer 4.5 in Windows Vista, Windows XP, Windows Server 2003 e Windows Server 2008. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




