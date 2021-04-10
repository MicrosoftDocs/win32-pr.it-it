---
title: Interfaccia ITsSbTargetEx
description: Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Interfaccia ITsSbTargetEx Servizi Desktop remoto
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964881"
---
# <a name="itssbtargetex-interface"></a>Interfaccia ITsSbTargetEx

Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.

Questa interfaccia è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato. La proprietà [**TargetLoad**](itssbtarget-targetload.md) dell'interfaccia [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) è disponibile a partire da Windows Server 2016.

## <a name="members"></a>Membri

L'interfaccia **ITsSbTargetEx** eredita da [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget). **ITsSbTargetEx** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **ITsSbTargetEx** ha queste proprietà.



| Proprietà                                                                      | Tipo di accesso           | Descrizione                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Lettura/Scrittura<br/> | Recupera o specifica il nome dell'ambiente associato alla destinazione.<br/> |
| [**Farmname**](itssbtarget-farmname.md)<br/>                           | Lettura/Scrittura<br/> | Specifica o Recupera il nome della farm a cui viene unita la destinazione.<br/>    |
| [**IpAddresses**](itssbtarget-ipaddresses.md)<br/>                     | Lettura/Scrittura<br/> | Recupera o specifica gli indirizzi IP esterni della destinazione.<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Sola lettura<br/>  | Recupera il numero di connessioni utente in sospeso per la destinazione.<br/>               |
| [**NumSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Sola lettura<br/>  | Recupera il numero di sessioni gestite da Service Broker per la destinazione.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Lettura/Scrittura<br/> | Specifica o Recupera il nome di dominio completo della destinazione.<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Sola lettura<br/>  | Recupera il carico relativo in una destinazione.<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | Lettura/Scrittura<br/> | Specifica o Recupera il nome della destinazione.<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Lettura/Scrittura<br/> | Specifica o Recupera il nome NetBIOS della destinazione.<br/>                         |
| [**TargetPropertySet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Lettura/Scrittura<br/> | Specifica o Recupera il set di proprietà per la destinazione.<br/>                        |
| [**TargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Lettura/Scrittura<br/> | Specifica o recupera lo stato di destinazione.<br/>                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                |
| Fine del supporto server<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx è definito come 74f99987-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Interfacce di virtualizzazione Desktop remoto](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

