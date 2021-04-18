---
description: La proprietà ACTION può essere impostata sui valori seguenti.
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: Proprietà ACTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329617"
---
# <a name="action-property"></a>Proprietà ACTION

La proprietà **Action** può essere impostata sui valori seguenti.

## <a name="value"></a>Valore



| Valore                                                                                                                                            | Significato                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**INSTALLARE**</dt> </dl>       | [Azione di installazione](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**PUBBLICIZZARE**</dt> </dl> | [Pubblicizza azione](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**ADMIN**</dt> </dl>             | [Azione di amministrazione](admin-action.md)<br/>         |



 

La proprietà **Action** determina l'azione da eseguire se viene fornito un nome di azione null a [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o al [**Metodo DoAction**](session-doaction.md). Se non viene definito alcun valore per la proprietà **Action** , il programma di installazione chiama l' [azione di installazione](install-action.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




