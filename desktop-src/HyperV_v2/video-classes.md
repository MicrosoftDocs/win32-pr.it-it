---
description: Tutte le macchine virtuali riflettono la presenza di un controller video S3 emulato e un controller video accelerato e sintetico.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classi video
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485693"
---
# <a name="video-classes"></a>Classi video

Tutte le macchine virtuali riflettono la presenza di un controller video S3 emulato e un controller video accelerato e sintetico.

A ogni controller di visualizzazione è associato un oggetto Head del video. In una macchina virtuale può essere attivo un solo controller di visualizzazione in qualsiasi momento.

È presente una connessione terminal per ogni sessione remota attiva connessa a una macchina virtuale.

Di seguito sono riportate le classi WMI di virtualizzazione correlate ai video.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                  | Descrizione                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_S3DisplayController MSVM**](msvm-s3displaycontroller.md)<br/>               | Rappresenta lo stato del controller S3 emulato presente in ogni configurazione di macchina virtuale.<br/>       |
| [**\_SyntheticDisplayController MSVM**](msvm-syntheticdisplaycontroller.md)<br/> | Rappresenta lo stato del controller di visualizzazione sintetico presente in ogni configurazione di macchina virtuale.<br/> |
| [**\_SystemTerminalConnection MSVM**](msvm-systemterminalconnection.md)<br/>     | Associa una macchina virtuale a una connessione terminale.<br/>                                                        |
| [**\_TerminalConnection MSVM**](msvm-terminalconnection.md)<br/>                 | Indica lo stato di una sessione remota attiva che interagisce con una macchina virtuale.<br/>                             |
| [**\_VideoHead MSVM**](msvm-videohead.md)<br/>                                   | Descrive la superficie di disegno principale in un controller di visualizzazione.<br/>                                                  |
| [**\_VideoHeadOnController MSVM**](msvm-videoheadoncontroller.md)<br/>           | Associa una testa video al controller video che lo include.<br/>                                             |



 

 

 




