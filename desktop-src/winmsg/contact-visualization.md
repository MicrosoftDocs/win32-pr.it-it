---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato un contatto di input.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualizzazione contatto (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348191"
---
# <a name="contact-visualization"></a>Visualizzazione contatto

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato un contatto di input.

Queste costanti vengono usate con i parametri **SPI \_ GETCONTACTVISUALIZATION** e **SPI \_ SETCONTACTVISUALIZATION** e la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ disattivato**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i contatti è disattivato.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i contatti è on.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**\_PRESENTATIONMODE CONTACTVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i contatti è acceso con gli oggetti visivi in modalità presentazione.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di configurazione](configuration-constants.md)
</dt> <dt>

[**Visualizzazione movimenti**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configurazione feedback input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

