---
description: La proprietà MSIARPSETTINGSIDENTIFIER contiene un elenco delimitato da punti e virgola dei percorsi del registro di sistema in cui l'applicazione archivia le impostazioni e le preferenze di un utente.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Proprietà MSIARPSETTINGSIDENTIFIER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331311"
---
# <a name="msiarpsettingsidentifier-property"></a>Proprietà MSIARPSETTINGSIDENTIFIER

La proprietà **MSIARPSETTINGSIDENTIFIER** contiene un elenco delimitato da punti e virgola dei percorsi del registro di sistema in cui l'applicazione archivia le impostazioni e le preferenze di un utente. Durante un aggiornamento del sistema operativo, il programma di installazione può utilizzare queste informazioni per migliorare l'esperienza degli utenti che eseguono la migrazione delle applicazioni.

Il valore della proprietà **MSIARPSETTINGSIDENTIFIER** è un testo letterale che contiene l'elenco dei percorsi del registro di sistema in cui vengono archiviate le impostazioni dell'applicazione. Il valore può specificare più percorsi del registro di sistema possibili. Separare più percorsi del registro di sistema usando un punto e virgola. Le impostazioni dell'applicazione vengono in genere archiviate negli hive del registro di sistema **HKCU** o **HKLM** nel formato: *\\ \\ versione dell'applicazione aziendale*. L'esempio seguente è un possibile valore per la proprietà **MSIARPSETTINGSIDENTIFIER** .

*MyCompany \\ AppSuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*

Questa proprietà è facoltativa e può essere impostata nella tabella delle [Proprietà](property-table.md) . Se questa proprietà viene visualizzata nella tabella delle proprietà, il valore non deve essere impostato su **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




