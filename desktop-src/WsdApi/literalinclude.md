---
description: Inserisce un'istruzione di inclusione C o IDL nel codice generato.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: elemento literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2701b2b21d14b629d5d9b61dcbc73e11371f54e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313151"
---
# <a name="literalinclude-element"></a>elemento literalInclude

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
<td>stringa lingua<br/></td>
<td>No<br/></td>
<td>Tipo di file di intestazione da includere. <br/> <br/>
<dt><strong>C</strong></dt> <dd> Includere un file di intestazione C.<br/> </dd> <dt><strong>IDL</strong></dt> <dd> Includere un file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Locale</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Questo attributo viene utilizzato solo quando la <strong>lingua</strong> è impostata su &quot; C &quot; .<br/> <br/>
<dt><strong>True</strong></dt> <dd> Cerca l'intestazione denominata nella directory corrente prima di cercare le directory di sistema.<br/> </dd> <dt><strong>False</strong></dt> <dd> Cerca solo le directory di sistema per l'intestazione denominata.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                         | Descrizione                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**file**](file.md)<br/> | Restituisce un file dal generatore di codice.<br/> <br/> |



## <a name="remarks"></a>Commenti

Negli esempi seguenti viene illustrato il codice generato da elementi **literalInclude** diversi.

### <a name="example-1---generating-a-c-include-statement"></a>Esempio 1: generazione di un'istruzione di inclusione C

XML di input:

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

Codice di output:

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a>Esempio 2: generazione di un'istruzione di inclusione C

XML di input:

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

Codice di output:

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a>Esempio 3: generazione di un'istruzione Import IDL

XML di input:

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

Codice di output:

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | Sì           |



 

 




