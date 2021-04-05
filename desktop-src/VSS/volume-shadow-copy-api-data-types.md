---
description: "I tipi di dati seguenti sono definiti nell'API copia shadow del volume:"
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipi di dati dell'API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751583"
---
# <a name="volume-shadow-copy-api-data-types"></a>Tipi di dati dell'API copia shadow del volume

I tipi di dati seguenti sono definiti nell'API copia shadow del volume:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>\_ID VSS
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

La definizione dell' **\_ ID VSS** specifica il formato generale dell'identificatore VSS. L' **\_ ID VSS** è un tipo di dati GUID standard.

Servizio Copia **shadow \_ del volume Gli ID** vengono utilizzati per identificare gli elementi seguenti: copie shadow, set di copie shadow, provider, versioni del provider, Writer (identificatore di classe del writer) e istanze di writer.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_PWSZ VSS
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

La definizione **VSS \_ PWSZ** specifica una stringa di caratteri wide a terminazione null (WCHAR).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_timestamp VSS
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

La definizione del **\_ timestamp VSS** contiene informazioni timestamp come valore integer a 64 bit contenente il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). Questa definizione è interscambiabile con la struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> </dl>

 

 
