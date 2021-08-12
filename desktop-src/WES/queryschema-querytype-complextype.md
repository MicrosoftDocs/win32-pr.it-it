---
title: Tipo complesso QueryType
description: Definisce un set di query di selettore e di eliminazione utilizzate per includere o escludere eventi dal set di risultati.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- EventLog di tipo complesso QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6585b43e1e9e48bc0be69001d471c74e52506177250d66316273ca447b38084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587626"
---
# <a name="querytype-complex-type"></a>Tipo complesso QueryType

Definisce un set di query di selettore e di eliminazione utilizzate per includere o escludere eventi dal set di risultati.

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                    | Tipo | Descrizione                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Selezionare**](queryschema-select-querytype-element.md)     |      | Query XPath che identifica gli eventi da includere nel set di risultati della query. Specificare l'XPath nel corpo del testo di questo elemento. XPath è limitato a 32 espressioni.<br/>   |
| [**Elimina**](queryschema-suppress-querytype-element.md) |      | Query XPath che identifica gli eventi da escludere dal set di risultati della query. Specificare l'XPath nel corpo del testo di questo elemento. XPath è limitato a 32 espressioni.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id   | long   | Identificatore che identifica in modo univoco la query nell'elenco di query. L'identificatore è in base zero. È necessario specificare un identificatore se l'elenco di query contiene più di una query.<br/> |
| Path | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/>                                                                                                            |
| Path | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/>                                                                                                            |
| Path | anyURI | Non usato.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Commenti

La query deve avere almeno un'istruzione select. Per ogni istruzione suppress deve essere presente almeno un'istruzione select che specifica lo stesso percorso. Se la query select e suppress restituiscono gli stessi eventi, l'istruzione suppress ha la precedenza. Se si selezionano eventi da più origini, gli eventi vengono restituiti in ordine di timestamp. Se si usa il timestamp di sistema e la frequenza degli eventi è elevata, è possibile che più di un evento abbia lo stesso timestamp. In questo caso, l'ordinamento degli eventi diventa ambiguo e gli eventi potrebbero risultare non in ordine.

Se si specifica un percorso per una delle query nell'elenco di query, tutte le query devono specificare un percorso. Se non si specifica un percorso per tutte le query, è necessario specificarne il percorso quando si chiama la [**funzione EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe.**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





