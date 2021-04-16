---
title: Tipo complesso FilterListType
description: Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Log eventi di tipo complesso FilterListType
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341213"
---
# <a name="filterlisttype-complex-type"></a>Tipo complesso FilterListType

Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento    | Tipo                                                             | Descrizione                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Elenco di filtri.<br/> |



## <a name="remarks"></a>Commenti

Un controller ETW è un'applicazione che chiama la funzione [**StartTrace**](/windows/desktop/ETW/starttrace) per creare una sessione ETW. Per informazioni dettagliate, vedere [controllo delle sessioni di traccia eventi](/windows/desktop/ETW/controlling-event-tracing-sessions). Il controller può utilizzare la funzione [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) per enumerare i filtri definiti. Il controller può quindi passare uno o più filtri quando chiama la funzione [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) per abilitare il provider. Il provider riceve i filtri, insieme al resto dei parametri enable, nella funzione di callback [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

