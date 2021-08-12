---
title: Tipo complesso FilterListType
description: Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- EventLog di tipo complesso FilterListType
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b66ccc002372159540895dfbe95786921266320bb4d3a4e6827085ae7822c12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589626"
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
| **filter** | [**Filtertype**](eventmanifestschema-filtertype-complextype.md) | Elenco di filtri.<br/> |



## <a name="remarks"></a>Commenti

Un controller ETW è un'applicazione che chiama la [**funzione StartTrace**](/windows/desktop/ETW/starttrace) per creare una sessione ETW. Per informazioni dettagliate, vedere [Controllo delle sessioni di traccia eventi](/windows/desktop/ETW/controlling-event-tracing-sessions). Il controller può usare [**la funzione TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) per enumerare i filtri definiti. Il controller può quindi passare uno o più filtri quando chiama la [**funzione EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) per abilitare il provider. Il provider riceve i filtri, insieme al resto dei parametri di abilitazione, nella funzione di callback [*EnableCallback.*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

