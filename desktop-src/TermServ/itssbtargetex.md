---
title: Interfaccia ITsSbTargetEx
description: Espone le proprietà che archiviano le informazioni di configurazione e stato relative a una destinazione.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Interfaccia ITsSbTargetEx Servizi Desktop remoto
- Interfaccia ITsSbTargetEx Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fb9be0e4cf5c0395efa93d308fdfa45362a7ac8919ab49a108700106aff6081b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989821"
---
# <a name="itssbtargetex-interface"></a>Interfaccia ITsSbTargetEx

Espone le proprietà che archiviano le informazioni di configurazione e stato relative a una destinazione.

Questa interfaccia è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato. La [**proprietà TargetLoad**](itssbtarget-targetload.md) dell'interfaccia [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) è disponibile a partire da Windows Server 2016.

## <a name="members"></a>Membri

**L'interfaccia ITsSbTargetEx** eredita da [**ITsSbTarget.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) **ITsSbTargetEx** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia ITsSbTargetEx** ha queste proprietà.



| Proprietà                                                                      | Tipo di accesso           | Descrizione                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Lettura/Scrittura<br/> | Recupera o specifica il nome dell'ambiente associato alla destinazione.<br/> |
| [**FarmName**](itssbtarget-farmname.md)<br/>                           | Lettura/Scrittura<br/> | Specifica o recupera il nome della farm a cui è unita la destinazione.<br/>    |
| [**Ipaddresses**](itssbtarget-ipaddresses.md)<br/>                     | Lettura/Scrittura<br/> | Recupera o specifica gli indirizzi IP esterni della destinazione.<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Sola lettura<br/>  | Recupera il numero di connessioni utente in sospeso per la destinazione.<br/>               |
| [**Sessioni NumSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Sola lettura<br/>  | Recupera il numero di sessioni gestite dal broker per la destinazione.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Lettura/Scrittura<br/> | Specifica o recupera il nome di dominio completo della destinazione.<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Sola lettura<br/>  | Recupera il carico relativo su una destinazione.<br/>                                       |
| [**Targetname**](itssbtarget-targetname.md)<br/>                       | Lettura/Scrittura<br/> | Specifica o recupera il nome della destinazione.<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Lettura/Scrittura<br/> | Specifica o recupera il nome NetBIOS della destinazione.<br/>                         |
| [**TargetPropertySet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Lettura/Scrittura<br/> | Specifica o recupera il set di proprietà per la destinazione.<br/>                        |
| [**Stato di destinazione**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Lettura/Scrittura<br/> | Specifica o recupera lo stato di destinazione.<br/>                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx è definito come 74f99987-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Desktop remoto virtualization interface](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

