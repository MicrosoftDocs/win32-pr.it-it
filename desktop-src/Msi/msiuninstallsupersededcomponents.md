---
description: Impostare la proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS su 1 nella tabella delle proprietà o su una riga di comando.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331069"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS

Impostare la proprietà **MSIUNINSTALLSUPERSEDEDCOMPONENTS** su 1 nella [tabella delle proprietà](property-table.md) o su una riga di comando. Quando questa proprietà è stata impostata su 1, il programma di installazione determina se i componenti in tutte le patch sostituite stanno diventando ridondanti. Il programma di installazione può annullare la registrazione e disinstallare i componenti ridondanti per evitare di lasciare i componenti orfani nel computer.

L'impostazione di questa proprietà influiscono sui componenti in tutte le patch sostituite. Per abilitare questa funzionalità per i singoli componenti, usare l'attributo **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md).

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Le versioni precedenti a Windows Installer 4,5 ignorano la proprietà **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,5 o Windows Installer 4,5 in Windows Vista, Windows XP, Windows Server 2003 e Windows Server 2008. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




