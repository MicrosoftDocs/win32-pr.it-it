---
description: PRIMARYFOLDER è una proprietà globale che consente all'autore di designare una cartella primaria per l'installazione.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Proprietà PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326259"
---
# <a name="primaryfolder-property"></a>Proprietà PRIMARYFOLDER

**PRIMARYFOLDER** è una proprietà globale che consente all'autore di designare una cartella primaria per l'installazione. Il valore di questa proprietà deve essere il nome della chiave di una directory presente nella [tabella di directory](directory-table.md).

Il programma di installazione usa il percorso risolto della cartella primaria per determinare il volume da usare per l'impostazione dei valori della proprietà [**PrimaryVolumePath**](primaryvolumepath.md) , della proprietà [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , della proprietà [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) e della proprietà [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) . Il programma di installazione fornisce i valori di queste ultime proprietà agli utenti nell'interfaccia utente per consentire la gestione dello spazio su disco. Gli autori di pacchetti di solito possono selezionare la cartella più grande come cartella primaria.

Il valore di questa proprietà deve essere il nome chiave di un record di directory trovato nella [tabella directory](directory-table.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




