---
title: Costanti WINBIO_FLAG (tipi WinBio \_ . h)
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
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400352"
---
# <a name="winbio_flag-constants"></a>\_Costanti flag WINBIO

Nella funzione [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) è possibile usare le costanti seguenti per specificare la configurazione di unità biometriche e le caratteristiche di accesso per la nuova sessione.



| Costante                                                                                                                                                                                     | Descrizione                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**\_impostazione predefinita del flag WINBIO \_**</dt> </dl>             | Flag di configurazione del sensore. Le unità biometriche operano nel modo specificato durante l'installazione.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**\_flag WINBIO \_ Basic**</dt> </dl>                   | Flag di configurazione del sensore. Le unità biometriche funzionano solo come dispositivi di acquisizione di base.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**\_flag WINBIO \_ avanzato**</dt> </dl>          | Flag di configurazione del sensore. Le unità biometriche usano le funzionalità di elaborazione e archiviazione interne.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**FLAG WINBIO non \_ \_ elaborato**</dt> </dl>                         | Flag di accesso desiderato. L'applicazione client acquisisce i dati biometrici non elaborati usando [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**\_manutenzione del flag WINBIO \_**</dt> </dl> | Flag di accesso desiderato. Il client esegue operazioni di controllo definite dal fornitore su un'unità biometrica chiamando [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





