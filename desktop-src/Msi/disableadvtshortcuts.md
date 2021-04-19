---
description: L'impostazione della proprietà DISABLEADVTSHORTCUTS Disabilita la generazione di collegamenti che supportano l'installazione su richiesta e l'annuncio. L'impostazione di questa proprietà specifica che questi tasti di scelta rapida devono essere sostituiti da collegamenti regolari.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Proprietà DISABLEADVTSHORTCUTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324246"
---
# <a name="disableadvtshortcuts-property"></a>Proprietà DISABLEADVTSHORTCUTS

L'impostazione della proprietà **DISABLEADVTSHORTCUTS** Disabilita la generazione di collegamenti che supportano l' [installazione su richiesta](installation-on-demand.md) e l' [annuncio](advertisement.md). L'impostazione di questa proprietà specifica che questi tasti di scelta rapida devono essere sostituiti da collegamenti regolari.

## <a name="default-value"></a>Valore predefinito

Per impostazione predefinita, la generazione del collegamento di installazione su richiesta è abilitata.

## <a name="remarks"></a>Commenti

I tasti di scelta rapida che supportano l'annuncio hanno il nome di una funzionalità, anziché un percorso di file formattato nel formato \[ \# FileKey \] , immessi nella colonna di destinazione della [tabella dei collegamenti](shortcut-table.md). Se questa proprietà è impostata e la funzionalità è installata, il programma di installazione genera un collegamento normale alla funzionalità.

Questa proprietà viene comunemente utilizzata dagli amministratori per gli utenti che eseguono il roaming tra ambienti che non supportano la pubblicità. Questa proprietà può essere impostata da una trasformazione, nel flusso amministrativo o nella [tabella delle proprietà](property-table.md). Se viene impostata tramite la riga di comando o tramite una chiamata a [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), è necessario reimpostarla di nuovo durante ogni successiva installazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




