---
title: Tipo complesso QueryType
description: Definisce un set di query di selezione e di eliminazione utilizzate per includere eventi in o escludere eventi dal set di risultati.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Log eventi di tipo complesso QueryType
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119682"
---
# <a name="querytype-complex-type"></a>Tipo complesso QueryType

Definisce un set di query di selezione e di eliminazione utilizzate per includere eventi in o escludere eventi dal set di risultati.

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
| [**Selezionare**](queryschema-select-querytype-element.md)     |      | Query XPath che identifica gli eventi da includere nel set di risultati della query. Specificare XPath nel corpo del testo di questo elemento. XPath è limitato a 32 espressioni.<br/>   |
| [**Elimina**](queryschema-suppress-querytype-element.md) |      | Query XPath che identifica gli eventi da escludere dal set di risultati della query. Specificare XPath nel corpo del testo di questo elemento. XPath è limitato a 32 espressioni.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id   | long   | Identificatore che identifica in modo univoco la query nell'elenco di query. L'identificatore è in base zero. È necessario specificare un identificatore se l'elenco di query contiene più di una query.<br/> |
| Percorso | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/>                                                                                                            |
| Percorso | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/>                                                                                                            |
| Percorso | anyURI | Non usato.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Commenti

La query deve contenere almeno un'istruzione SELECT. Per ogni istruzione di eliminazione, è necessario che sia presente almeno un'istruzione SELECT che specifica lo stesso percorso. Se la query di selezione e di eliminazione restituisce gli stessi eventi, l'istruzione di eliminazione avrà la precedenza. Se si selezionano eventi da più origini, gli eventi vengono restituiti nell'ordine del timestamp. Se si usa l'indicatore di ora di sistema e la frequenza degli eventi è elevata, è possibile che più di un evento disponga dello stesso timestamp. Quando si verifica questa situazione, l'ordine degli eventi diventa ambiguo e gli eventi potrebbero non essere visualizzati in ordine.

Se si specifica un percorso per una delle query nell'elenco di query, tutte le query devono specificare un percorso. Se non si specifica un percorso per tutte le query, è necessario specificare il percorso quando si chiama la funzione [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





