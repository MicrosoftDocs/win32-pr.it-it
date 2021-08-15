---
description: La proprietà Intel viene impostata dal programma di Windows sul livello del processore numerico quando viene eseguito in un processore Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Proprietà Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5b4fe488867a67da1f97ce4564bb8ce530b89417554a91a8734bee6e863f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013239"
---
# <a name="intel-property"></a>Proprietà Intel

La **proprietà Intel** viene impostata dal Windows installer sul livello del processore numerico quando è in esecuzione su un processore Intel. I valori sono gli stessi del *campo wProcessorLevel* della [**struttura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) Quando viene eseguito in un processore x64, il programma di installazione di Windows imposta la proprietà **Intel** in modo che rifletta il processore x86 emulato dal computer x64 come segnalato dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
