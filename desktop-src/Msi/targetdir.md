---
description: La proprietà TARGETDIR specifica la directory di destinazione radice per l'installazione.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: Proprietà TARGETDIR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329952"
---
# <a name="targetdir-property"></a>Proprietà TARGETDIR

La proprietà **targetdir** specifica la directory di destinazione radice per l'installazione. **Targetdir** deve essere il nome di una radice nella tabella [directory](directory-table.md) . Può essere presente una sola directory di destinazione radice. Durante un' [installazione amministrativa](administrative-installation.md) questa proprietà specifica il percorso in cui copiare il pacchetto di installazione. Durante un'installazione non amministrativa questa proprietà specifica la directory di destinazione radice.

Per specificare la directory di destinazione radice, impostare la colonna directory della tabella directory sulla proprietà **targetdir** e la colonna DefaultDir sulla proprietà [**SourceDir**](sourcedir.md) . Se la proprietà **targetdir** è definita, la directory di destinazione viene risolta nel valore della proprietà. Se la proprietà **targetdir** è indefinita, per risolvere il percorso viene utilizzata la proprietà [**ROOTDRIVE**](rootdrive.md) . Per ulteriori informazioni sull'utilizzo della proprietà **targetdir** , vedere [utilizzo della tabella directory](using-the-directory-table.md).

Si noti che il valore della proprietà **targetdir** viene in genere impostato dalla riga di comando o tramite un'interfaccia utente. L'impostazione di **targetdir** tramite la creazione di un percorso nella [tabella delle proprietà](property-table.md) non è consigliata perché i computer sono diversi nella configurazione dell'unità locale.

Per ulteriori informazioni su come modificare TARGETDIR durante un'installazione, vedere [modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




