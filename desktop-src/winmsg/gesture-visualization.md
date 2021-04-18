---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti elencati.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualizzazione movimenti (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317238"
---
# <a name="gesture-visualization"></a>Visualizzazione movimenti

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare il modo in cui viene elaborato il feedback dell'interfaccia utente quando viene rilevato uno dei movimenti elencati.

Queste costanti vengono usate con i parametri **SPI \_ GETGESTUREVISUALIZATION** e **SPI \_ SETGESTUREVISUALIZATION** e la funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .

**Nota**  

Per recuperare o impostare le informazioni di visualizzazione della penna, è consigliabile usare i parametri **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e le costanti elencate nella [**visualizzazione Pen**](pen-visualization.md).

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ disattivato**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti è disattivato.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti è on.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**\_tocco GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Specifica il feedback dell'interfaccia utente per il tocco.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**\_DOUBLETAP GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un doppio tocco.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**\_PRESSANDTAP GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Specifica il feedback dell'interfaccia utente per una pressione e un tocco.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**\_PRESSANDHOLD GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Specifica il feedback dell'interfaccia utente per una pressione e un tasto di attesa.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**\_RIGHTTAP GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Specifica il feedback dell'interfaccia utente per il tocco corretto.


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

[**Visualizzazione contatto**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configurazione feedback input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

