---
description: Inserisce un'istruzione di inclusione C o IDL nel codice generato.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: Elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995128"
---
# <a name="literalinclude-element"></a>Elemento literalInclude

Inserisce un'istruzione di inclusione C o IDL nel codice generato.

## <a name="usage"></a>Utilizzo

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Lingua</strong><br/></td>
<td>stringa del linguaggio<br/></td>
<td>No<br/></td>
<td>Tipo di file di intestazione da includere. <br/> <br/>
<dt><strong>C</strong></dt> <dd> Includere un file di intestazione C.<br/> </dd> <dt><strong>Idl</strong></dt> <dd> Includere un file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Locale</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Questo attributo viene usato solo quando <strong>Language</strong> è impostato su &quot; C &quot; .<br/> <br/>
<dt><strong>Vero</strong></dt> <dd> Cerca l'intestazione denominata nella directory corrente prima di cercare le directory di sistema.<br/> </dd> <dt><strong>False</strong></dt> <dd> Cercare solo le directory di sistema per l'intestazione denominata.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**ﬁle**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Gli esempi seguenti illustrano il codice generato da **diversi elementi literalInclude.**

### <a name="example-1---generating-a-c-include-statement"></a>Esempio 1 - Generazione di un'istruzione C include

XML di input:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Codice di output:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Esempio 2 - Generazione di un'istruzione C include

XML di input:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Codice di output:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Esempio 3 - Generazione di un'istruzione IDL import

XML di input:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Codice di output:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Informazioni sull'elemento



| Label | Valore |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




