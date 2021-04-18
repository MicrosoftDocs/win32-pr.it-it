---
title: Visualizza scriptFile
description: L'attributo scriptFile specifica i nomi file dei file JScript associati.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- Visualizza Media Player Windows scriptFile
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330886"
---
# <a name="viewscriptfile"></a>Visualizza scriptFile

L'attributo **scriptFile** specifica i nomi file dei file JScript associati.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di sola scrittura senza valore predefinito. I nomi file di più file JScript sono delimitati da punti e virgola. Gli spazi iniziali e successivi e i punti e virgola non devono essere presenti.

## <a name="remarks"></a>Commenti

Il codice nei file specificati può essere utilizzato da qualsiasi gestore eventi nella vista. Il codice usato dai gestori eventi in più visualizzazioni può essere inserito in un file con lo stesso nome del file di definizione dell'interfaccia, ma con un'estensione js anziché un'estensione WMS. Questo file viene caricato automaticamente e non deve essere specificato nel file di definizione dell'interfaccia.

## <a name="examples"></a>Esempio


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





