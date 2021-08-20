---
description: Il Windows di installazione imposta la proprietà OriginalDatabase sul percorso del database di installazione usato per avviare l'installazione.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: OriginalDatabase - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b8ec6b77d013ee89d081c0ff20e3ad00750454e1fa9299d364fdb94e69ccb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145534"
---
# <a name="originaldatabase-property"></a>OriginalDatabase - proprietà

Il Windows di installazione imposta **la proprietà OriginalDatabase** sul percorso del database di installazione usato per avviare l'installazione. Se l'installazione viene avviata da una riga di comando, il valore dipende dal fatto che l'opzione del pacchetto recache (il flag -v) sia presente nella [**proprietà REINSTALLMODE.**](reinstallmode.md)



| Metodo di installazione                                                                                                                                                                                  | Valore OriginalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Qualsiasi installazione avviata richiamando il percorso del pacchetto di installazione (.msi file).                                                                                                              | Percorso del pacchetto di installazione (.msi file). |
| Installazione avviata dalla riga di comando. L'installazione non viene avviata da un percorso del pacchetto. L'opzione recache (flag -v) è presente nella [**proprietà REINSTALLMODE.**](reinstallmode.md)     | Percorso del database nell'origine.           |
| Installazione avviata dalla riga di comando. L'installazione non viene avviata da un percorso del pacchetto. L'opzione recache (flag -v) non è presente nella [**proprietà REINSTALLMODE.**](reinstallmode.md) | Percorso del database memorizzato nella cache.                  |



 

## <a name="remarks"></a>Commenti

Durante la prima installazione, un'azione personalizzata sequenziata prima dell'azione [ResolveSource](resolvesource-action.md) può usare la proprietà **OriginalDatabase** per determinare il percorso dell'origine dell'installazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




