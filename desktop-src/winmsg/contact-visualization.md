---
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione del feedback dell'interfaccia utente quando viene rilevato un contatto di input.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualizzazione contatti (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea196017b1731bb176cd21a7dc02aaa360f4fe70503bd204b9c488d38eff99ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437254"
---
# <a name="contact-visualization"></a>Visualizzazione dei contatti

Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione del feedback dell'interfaccia utente quando viene rilevato un contatto di input.

Queste costanti vengono usate con i parametri **SPI \_ GETCONTACTMETRIC** e **SPI \_ SETCONTACTMETRIC** e la [**funzione SystemParametersInfo.**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**\_CONTACTVISUALIZZAZIONE DISATTIVATA**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Specifica che il feedback dell'interfaccia utente per tutti i contatti è disattivato.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**\_CONTACTVISUALIZZAZIONE ON**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Specifica il feedback dell'interfaccia utente per tutti i contatti.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**MODALITÀ PRESENTAZIONE \_ CONTACTVISUALIZZAZIONE**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Specifica il feedback dell'interfaccia utente per tutti i contatti è attiva con oggetti visivi in modalità presentazione.


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

[**Visualizzazione movimenti**](gesture-visualization.md)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Configurazione dei commenti e suggerimenti sull'input](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

