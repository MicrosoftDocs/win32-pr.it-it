---
description: La proprietà ACTION può essere impostata su questi valori.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b4f17c7bd08b2e366fa23a55ad2b8044ce845ac4df04d0164ba34ad6dff32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145994"
---
# <a name="action-property"></a>ACTION - proprietà

La **proprietà ACTION** può essere impostata su questi valori.

## <a name="value"></a>Valore



| Valore                                                                                                                                            | Significato                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**Installare**</dt> </dl>       | [Azione INSTALL](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**Pubblicizzare**</dt> </dl> | [AZIONE ADVERTISE](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**Admin**</dt> </dl>             | [Azione ADMIN](admin-action.md)<br/>         |



 

La **proprietà ACTION** determina l'azione da eseguire se viene fornito un nome di azione Null a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o al metodo [**DoAction**](session-doaction.md). Se non è definito alcun valore per la **proprietà ACTION,** il programma di installazione chiama l'azione [INSTALL](install-action.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




