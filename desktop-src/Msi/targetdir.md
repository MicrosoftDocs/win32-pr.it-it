---
description: La proprietà TARGETDIR specifica la directory di destinazione radice per l'installazione.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b61575de21b47b1d82764d96e5876a9fd4c89fb1f837150988aa2c7a08e07be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626601"
---
# <a name="targetdir-property"></a>TARGETDIR - proprietà

La **proprietà TARGETDIR** specifica la directory di destinazione radice per l'installazione. **TARGETDIR** deve essere il nome di una radice nella [tabella Directory.](directory-table.md) Può essere presente una sola directory di destinazione radice. Durante [un'installazione amministrativa](administrative-installation.md) questa proprietà specifica il percorso in cui copiare il pacchetto di installazione. Durante un'installazione non amministrativa questa proprietà specifica la directory di destinazione radice.

Per specificare la directory di destinazione radice, impostare la colonna Directory della tabella Directory sulla proprietà **TARGETDIR** e la colonna DefaultDir sulla [**proprietà SourceDir.**](sourcedir.md) Se la **proprietà TARGETDIR** è definita, la directory di destinazione viene risolta nel valore della proprietà. Se la **proprietà TARGETDIR** non è definita, la [**proprietà ROOTDRIVE**](rootdrive.md) viene usata per risolvere il percorso. Per altre informazioni sull'uso della **proprietà TARGETDIR,** vedere [Uso della tabella directory](using-the-directory-table.md).

Si noti che il valore della **proprietà TARGETDIR** viene in genere impostato nella riga di comando o tramite un'interfaccia utente. **L'impostazione di TARGETDIR** tramite la creazione di un percorso nella tabella [Proprietà non](property-table.md) è consigliata perché i computer differiscono nella configurazione dell'unità locale.

Per altre informazioni su come modificare TARGETDIR durante un'installazione, vedere [Modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




