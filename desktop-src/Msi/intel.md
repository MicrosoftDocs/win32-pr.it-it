---
description: La proprietà Intel viene impostata dal Windows Installer al livello di processore numerico durante l'esecuzione in un processore Intel.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Proprietà Intel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329748"
---
# <a name="intel-property"></a>Proprietà Intel

La proprietà **Intel** viene impostata dal Windows Installer al livello di processore numerico durante l'esecuzione in un processore Intel. I valori corrispondono al campo *wProcessorLevel* della struttura delle informazioni di [**sistema \_**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) . Quando è in esecuzione in un processore x64, il Windows Installer imposta la proprietà **Intel** in modo da riflettere il processore x86 emulato dal computer x64 come riportato dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
