---
title: Metodo AgeAllRecords della classe MicrosoftDNS_Zone
description: Il metodo AgeAllRecords consente la durata per alcuni o tutti i record non NS e non SOA in una zona.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- DNS del metodo AgeAllRecords
- DNS del metodo AgeAllRecords, classe MicrosoftDNS_Zone
- Classe MicrosoftDNS_Zone DNS, metodo AgeAllRecords
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478478"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a>Metodo AgeAllRecords della classe di \_ zona MicrosoftDNS

Il metodo **AgeAllRecords** consente la durata per alcuni o tutti i record non NS e non SOA in una zona.

## <a name="syntax"></a>Sintassi


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NodeName* \[ in, facoltativo\]
</dt> <dd>

Nome del nodo da Age.

</dd> <dt>

*ApplyToSubtree* \[ in, facoltativo\]
</dt> <dd>

Specifica se la durata deve essere applicata a tutti i record nel sottoalbero. Impostare su TRUE per applicare l'invecchiamento a tutti i record nel sottoalbero, iniziando con nodeName.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

ERRORE \_ indica che la durata è stata completata correttamente. Qualsiasi altro valore è un codice di errore.

## <a name="remarks"></a>Commenti

Se *NodeName* non è specificato, tutti i record saranno soggetti a durata e scavenging.

Se si specifica *NodeName* e *ApplyToSubtree* non è specificato o è impostato su zero, i record nel nodo specificato verranno sottoposti a tempo e scavenging.

Se si specifica *NodeName* e *ApplyToSubtree* è impostato su 1, tutti i record del sottoalbero a partire da *NodeName* verranno sottoposti a invecchiamento e scavenging. Il timestamp è impostato sull'ora corrente per tutti i record non NS e non SOA con i nomi del proprietario identificati dai parametri di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Zona MicrosoftDNS**](microsoftdns-zone.md)
</dt> <dt>

[**Metodo ChangeZoneType della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Metodo CreateZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**Metodo ForceRefresh della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Metodo getdistinguishname della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Metodo PauseZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Metodo ReloadZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Metodo ResetSecondaries della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[**Metodo ResumeZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Metodo UpdateFromDS della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**Metodo WriteBackZone della classe di \_ zona MicrosoftDNS**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





