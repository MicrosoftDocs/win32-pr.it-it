---
description: L'impostazione della proprietà DISABLEADVTSHORTCUTS disabilita la generazione di collegamenti che supportano l'installazione su richiesta e l'annuncio. L'impostazione di questa proprietà specifica che questi tasti di scelta rapida devono essere sostituiti da collegamenti normali.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: DISABLEADVTSHORTCUTS - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fd8465620abab56ebfe18f68254bf6d29b6e752a7550157231a0b1abe95ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745561"
---
# <a name="disableadvtshortcuts-property"></a>DISABLEADVTSHORTCUTS - proprietà

**L'impostazione della proprietà DISABLEADVTSHORTCUTS** disabilita la generazione di collegamenti che supportano [l'installazione su richiesta](installation-on-demand.md) e l'annuncio. [](advertisement.md) L'impostazione di questa proprietà specifica che questi tasti di scelta rapida devono essere sostituiti da collegamenti normali.

## <a name="default-value"></a>Valore predefinito

Per impostazione predefinita, la generazione di collegamenti su richiesta per l'installazione è abilitata.

## <a name="remarks"></a>Commenti

I collegamenti che supportano l'annuncio hanno il nome di una funzionalità, anziché un percorso di file formattato nel formato \[ \# filekey, immesso nella colonna Destinazione della tabella \] [Collegamento](shortcut-table.md). Se questa proprietà è impostata e la funzionalità è installata, il programma di installazione genera un collegamento regolare alla funzionalità.

Questa proprietà viene in genere usata dagli amministratori per gli utenti che si trovano in roaming tra ambienti che supportano e non supportano la pubblicità. Questa proprietà può essere impostata da una trasformazione, nel flusso amministrativo o nella [tabella Property](property-table.md). Se viene impostata tramite la riga di comando o tramite una chiamata a [**MsiSetProperty,**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)è necessario reimpostarla nuovamente durante ogni installazione successiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




