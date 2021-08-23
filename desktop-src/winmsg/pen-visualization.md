---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione del feedback dell'interfaccia utente quando viene rilevato uno dei movimenti della penna elencati.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualizzazione penna (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60b9f75493a361cc167b65fba1783bc01f909d76211b1076e2faccc2e6f00116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548491"
---
# <a name="pen-visualization"></a>Visualizzazione penna

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione del feedback dell'interfaccia utente quando viene rilevato uno dei movimenti della penna elencati.

Queste costanti vengono usate con i parametri **SPI \_ GETPENNTASSI** e **SPI \_ SETPENMETRIC** e la [**funzione SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**\_PENVISUALIZZAZIONE DISATTIVATA**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti della penna è disattivato.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**\_PENVISUALIZZAZIONE ON**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i movimenti della penna è on.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**TOCCO \_ PENVISUALIZZAZIONE**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Specifica il feedback dell'interfaccia utente per il tocco con penna.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PEN KPI \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Specifica il feedback dell'interfaccia utente per un doppio tocco della penna.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_PENVISUALIZZAZIONE CURSORE**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Specifica il feedback dell'interfaccia utente per il cursore penna.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                 |
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

 

