---
description: La proprietà DefaultUIFont imposta lo stile del carattere predefinito usato per i controlli. Per specificare il valore predefinito, impostare DefaultUIFont su uno degli stili predefiniti nella tabella TextStyle della tabella Property.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: DefaultUIFont - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46bf4c432a0e75c933136cc11e1dd8a55cc6a4cdf2f09c923804132b743e88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289581"
---
# <a name="defaultuifont-property"></a>DefaultUIFont - proprietà

La **proprietà DefaultUIFont** imposta lo stile del carattere predefinito usato per i controlli. Per specificare il valore predefinito, **impostare DefaultUIFont** su uno degli stili predefiniti nella tabella [TextStyle](textstyle-table.md) della [tabella Property](property-table.md).

## <a name="remarks"></a>Commenti

La **proprietà DefaultUIFont** di ogni pacchetto di installazione con interfaccia utente deve essere impostata nella tabella [Proprietà](property-table.md) su uno degli stili predefiniti elencati nella [tabella TextStyle](textstyle-table.md). Se questa proprietà non viene specificata, il programma di installazione usa il tipo di carattere System. Ciò può causare la visualizzazione non corretta delle stringhe di testo da parte del programma di installazione quando la tabella codici del pacchetto è diversa dalla tabella codici predefinita dell'interfaccia utente dell'utente.

Il testo e lo stile del carattere di un controllo possono essere impostati come descritto in [Aggiunta di controlli e testo](adding-controls-and-text.md). Se la stringa di caratteri elencata nella colonna Text della tabella [Control](control-table.md) o della tabella [BBControl](bbcontrol-table.md) non specifica lo stile del carattere, il controllo usa il valore della **proprietà DefaultUIFont** come stile del carattere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




