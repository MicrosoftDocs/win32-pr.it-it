---
description: ICE52 verifica la presenza di proprietà private nella tabella AppSearch. Vedere informazioni sulle proprietà.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785dd468aaa637df02b9eb432dd77f9226d828a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883934"
---
# <a name="ice52"></a>ICE52

ICE52 verifica la presenza di proprietà private nella [tabella AppSearch](appsearch-table.md). Vedere [informazioni sulle proprietà](about-properties.md).

Quando si usa Windows 2000 tutte le proprietà impostate nella colonna proprietà della tabella AppSearch devono essere proprietà pubbliche.

## <a name="result"></a>Risultato

ICE52 pubblica un avviso se nella tabella AppSearch è presente una proprietà privata.

## <a name="example"></a>Esempio

ICE52 invia l'avviso seguente per l'esempio illustrato.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[Tabella AppSearch](appsearch-table.md)



| Proprietà  | Firma  |
|-----------|------------|
| PROPERTY1 | Signature1 |
| Property2 | Signature2 |



 

Per correggere questa modifica di avviso nella proprietà pubblica personalizzata: PROPERTY2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



