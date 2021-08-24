---
title: VIEW.scriptFile
description: L'attributo scriptFile specifica i nomi dei file JScript file.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- View.scriptFile Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f22b0fb5f0815c8977a363c033d26c0d68f725e0cdcd546bc2f2c1a7b723c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615331"
---
# <a name="viewscriptfile"></a>VIEW.scriptFile

**L'attributo scriptFile** specifica i nomi dei file JScript file.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di sola **scrittura** senza alcun valore predefinito. I nomi file di più JScript sono delimitati da punti e virgola. Gli spazi iniziali e seguenti e i punti e virgola non devono essere presenti.

## <a name="remarks"></a>Commenti

Il codice nei file specificati può essere usato da qualsiasi gestore eventi nella visualizzazione. Il codice usato dai gestori eventi in più visualizzazioni può essere inserito in un file con lo stesso nome del file di definizione dell'interfaccia, ma con estensione .js anziché wms. Questo file viene caricato automaticamente e non deve essere specificato nel file di definizione dell'interfaccia.

## <a name="examples"></a>Esempio


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





