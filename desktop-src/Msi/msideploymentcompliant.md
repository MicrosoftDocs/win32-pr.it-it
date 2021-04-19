---
description: È possibile impostare la proprietà MSIDEPLOYMENTCOMPLIANT per indicare al programma di installazione che il pacchetto è stato creato e testato per la conformità al controllo dell'account utente (UAC) in Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Proprietà MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329342"
---
# <a name="msideploymentcompliant-property"></a>Proprietà MSIDEPLOYMENTCOMPLIANT

È possibile impostare la proprietà **MSIDEPLOYMENTCOMPLIANT** per indicare al programma di installazione che il pacchetto è stato creato e testato per la conformità al [*controllo dell'account utente*](u-gly.md) (UAC) in Windows Vista. Se questa proprietà non è impostata, il programma di installazione di determinerà se il pacchetto è conforme al controllo dell'account utente in Windows Vista.

Per ulteriori informazioni su UAC e Windows Installer, vedere [utilizzo di Windows Installer con UAC](using-windows-installer-with-uac.md) e [linee guida per i pacchetti](guidelines-for-packages.md).

**Windows Installer 3,1, Windows Installer 3,0 e Windows Installer 2,0:** Questa proprietà viene ignorata. Questa proprietà viene utilizzata solo da Windows Installer 4,0 in Windows Vista.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Per informazioni sul Service Pack minimo richiesto da una versione Windows Installer, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




