---
description: Il programma di installazione imposta la proprietà AFTERREBOOT su 1 dopo un riavvio richiamato dall'azione ForceReboot. Il programma di installazione aggiunge AFTERREBOOT = 1 alla riga di comando eseguita subito dopo il riavvio.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Proprietà AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331620"
---
# <a name="afterreboot-property"></a>Proprietà AFTERREBOOT

Il programma di installazione imposta la proprietà **AFTERREBOOT** su 1 dopo un riavvio richiamato dall' [azione ForceReboot](forcereboot-action.md). Il programma di installazione aggiunge AFTERREBOOT = 1 alla riga di comando eseguita subito dopo il riavvio.

## <a name="remarks"></a>Commenti

L' [azione ForceReboot](forcereboot-action.md) deve sempre essere utilizzata con un'istruzione condizionale in modo tale che il programma di installazione avvii un riavvio solo quando necessario. Potrebbe essere necessario riavviare il computer se è stato sostituito un particolare file o se è stato installato un particolare componente. Il caso è diverso per ogni prodotto ed è possibile che sia necessaria un'azione personalizzata per determinare se è necessario riavviare il computer. La condizione sull'azione ForceReboot USA in genere la proprietà **AFTERREBOOT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Riavvio del sistema](system-reboots.md)
</dt> </dl>

 

 




