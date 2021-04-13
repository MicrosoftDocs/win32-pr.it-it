---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti penna elencati.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualizzazione penna (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529161"
---
# <a name="pen-visualization"></a>Visualizzazione penna

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti penna elencati.

Queste costanti vengono usate con i parametri **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ disattivato**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti di penna è disattivato.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti di penna è on.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**\_tocco PENVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un tocco della penna.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**\_DOUBLETAP PENVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un tocco di penna doppio.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_cursore PENVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Specifica il feedback dell'interfaccia utente per il cursore della penna.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di configurazione](configuration-constants.md)
</dt> <dt>

[**Visualizzazione contatto**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configurazione feedback input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

