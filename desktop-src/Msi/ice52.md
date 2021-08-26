---
description: ICE52 verifica la presenza di proprietà private nella tabella AppSearch. Vedere Informazioni sulle proprietà.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96f514f38e44a802b092acff53ac14f10c5e5d32c03888b7d45540443d34be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044041"
---
# <a name="ice52"></a>ICE52

ICE52 verifica la presenza di proprietà private nella [tabella AppSearch](appsearch-table.md). Vedere [Informazioni sulle proprietà](about-properties.md).

Quando si Windows 2000, tutte le proprietà impostate nella colonna Proprietà della tabella AppSearch devono essere proprietà pubbliche.

## <a name="result"></a>Risultato

ICE52 invia un avviso se è presente una proprietà privata nella tabella AppSearch.

## <a name="example"></a>Esempio

ICE52 pubblica l'avviso seguente per l'esempio illustrato.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[Tabella AppSearch](appsearch-table.md)



| Proprietà  | Firma  |
|-----------|------------|
| PROPERTY1 | Firma1 |
| Proprietà2 | Firma2 |



 

Per correggere questo avviso, passare alla proprietà pubblica personalizzata PROPERTY2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



