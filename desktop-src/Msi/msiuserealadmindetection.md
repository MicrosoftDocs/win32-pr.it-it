---
description: Impostare la proprietà MSIUSEREALADMINDETECTION su 1 per richiedere che il programma di installazione usi le informazioni utente effettive durante l'impostazione della proprietà AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: MSIUSEREALADMINDETECTION - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a177d320aff25cf21b932ca25e691f145f94ad3
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812934"
---
# <a name="msiuserealadmindetection-property"></a>MSIUSEREALADMINDETECTION - proprietà

Impostare la **proprietà MSIUSEREALADMINDETECTION** su 1 per richiedere che il programma di installazione usi le informazioni utente effettive durante l'impostazione [**della proprietà AdminUser.**](adminuser.md) Quando si esegue Windows Vista, [**Privileged**](privileged.md) e **AdminUser** sono uguali. Gli autori devono usare **la proprietà Privileged** nei nuovi pacchetti. I pacchetti legacy che richiedono **proprietà Privileged** e **AdminUser** distinte possono ripristinare la differenza impostando la **proprietà MSIUSEREALADMINDETECTION.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




