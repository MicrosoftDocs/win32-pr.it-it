---
description: La proprietà DefaultUIFont imposta lo stile del carattere predefinito usato per i controlli. Per specificare l'impostazione predefinita, impostare DefaultUIFont su uno degli stili predefiniti nella tabella TextStyle della tabella delle proprietà.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Proprietà DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333981"
---
# <a name="defaultuifont-property"></a>Proprietà DefaultUIFont

La proprietà **DefaultUIFont** imposta lo stile del carattere predefinito usato per i controlli. Per specificare l'impostazione predefinita, impostare **DefaultUIFont** su uno degli stili predefiniti nella [tabella TextStyle](textstyle-table.md) della [tabella delle proprietà](property-table.md).

## <a name="remarks"></a>Commenti

È necessario impostare la proprietà **DefaultUIFont** di ogni pacchetto di installazione con un'interfaccia utente nella [tabella delle proprietà](property-table.md) su uno degli stili predefiniti elencati nella [tabella TextStyle](textstyle-table.md). Se questa proprietà non è specificata, il programma di installazione utilizza il tipo di carattere di sistema. Questo può causare la visualizzazione non corretta delle stringhe di testo del programma di installazione quando la tabella codici del pacchetto è diversa dalla tabella codici dell'interfaccia utente predefinita dell'utente.

Il testo e lo stile del carattere di un controllo possono essere impostati come descritto in [aggiunta di controlli e testo](adding-controls-and-text.md). Se la stringa di caratteri elencata nella colonna di testo della tabella di [controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md) non specifica lo stile del tipo di carattere, il controllo utilizzerà il valore della proprietà **DefaultUIFont** come stile del tipo di carattere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




