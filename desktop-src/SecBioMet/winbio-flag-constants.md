---
title: WINBIO_FLAG costanti (Winbio \_ types.h)
description: Specificare la configurazione dell'unità biometrica e le caratteristiche di accesso per la nuova sessione.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e018b1d810e3a57b4adea1116aa9bebc7b82dd44888b2d720e018329d31acf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910311"
---
# <a name="winbio_flag-constants"></a>Costanti FLAG \_ WINBIO

Le costanti seguenti possono essere usate nella [**funzione WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) per specificare la configurazione dell'unità biometrica e le caratteristiche di accesso per la nuova sessione.



| Costante                                                                                                                                                                                     | Descrizione                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA DEL FLAG WINBIO \_ \_**</dt> </dl>             | Flag di configurazione del sensore. Le unità biometriche funzionano nel modo specificato durante l'installazione.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**WINBIO \_ FLAG \_ BASIC**</dt> </dl>                   | Flag di configurazione del sensore. Le unità biometriche funzionano solo come dispositivi di acquisizione di base.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**FLAG WINBIO \_ \_ AVANZATO**</dt> </dl>          | Flag di configurazione del sensore. Le unità biometriche usano le funzionalità di elaborazione e archiviazione interne.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**FLAG WINBIO \_ \_ NON ELABORATO**</dt> </dl>                         | Flag di accesso desiderato. L'applicazione client acquisisce dati biometrici non elaborati [**usando WinBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**MANUTENZIONE DEI FLAG WINBIO \_ \_**</dt> </dl> | Flag di accesso desiderato. Il client esegue operazioni di controllo definite dal fornitore su un'unità biometrica chiamando [**WinBioControlUnitPrivileged.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





