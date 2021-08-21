---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione del feedback dell'interfaccia utente quando viene rilevato uno dei movimenti elencati.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualizzazione movimenti (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f572addf2ad7a98dbe3afc63c69a305ea15546e9533918d952271372cf52b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849820"
---
# <a name="gesture-visualization"></a>Visualizzazione movimenti

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione del feedback dell'interfaccia utente quando viene rilevato uno dei movimenti elencati.

Queste costanti vengono usate con i parametri **SPI \_ GETGESTUREVISUALIZATION** e **SPI \_ SETGESTUREVISUALIZATION** e la [**funzione SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

**Nota**  

Per recuperare o impostare le informazioni di visualizzazione della penna, è consigliabile usare i parametri **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e le costanti elencate in [**Visualizzazione penna**](pen-visualization.md).

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti è disattivato.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti è on.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**TOCCO \_ GESTUREVISUALIZATION**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un tocco.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un doppio tocco.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Specifica il feedback dell'interfaccia utente per una pressione e un tocco.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Specifica il feedback dell'interfaccia utente per una pressione di pressione.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un tocco destro.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di configurazione](configuration-constants.md)
</dt> <dt>

[**Visualizzazione dei contatti**](contact-visualization.md)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configurazione dei commenti e suggerimenti sull'input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

