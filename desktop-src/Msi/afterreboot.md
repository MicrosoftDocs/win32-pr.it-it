---
description: Il programma di installazione imposta la proprietà AFTERREBOOT su 1 dopo un riavvio richiamato dall'azione ForceReboot. Il programma di installazione aggiunge AFTERREBOOT=1 alla riga di comando eseguita immediatamente dopo il riavvio.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: AFTERREBOOT - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8fb80a3d8ff167f93aab6c95fc3eadb8b5312daf9d2a2856f01cb7d01ee383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145914"
---
# <a name="afterreboot-property"></a>AFTERREBOOT - proprietà

Il programma di installazione imposta **la proprietà AFTERREBOOT** su 1 dopo un riavvio richiamato dall'azione [ForceReboot](forcereboot-action.md). Il programma di installazione aggiunge AFTERREBOOT=1 alla riga di comando eseguita immediatamente dopo il riavvio.

## <a name="remarks"></a>Commenti

[L'azione ForceReboot](forcereboot-action.md) deve sempre essere usata con un'istruzione condizionale in modo che il programma di installazione attiva un riavvio solo quando necessario. Potrebbe essere necessario un riavvio se un file specifico è stato sostituito o se è stato installato un componente specifico. Il caso è diverso per ogni prodotto e potrebbe essere necessaria un'azione personalizzata per determinare se è necessario un riavvio. La condizione nell'azione ForceReboot usa in genere la **proprietà AFTERREBOOT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Riavvii del sistema](system-reboots.md)
</dt> </dl>

 

 




