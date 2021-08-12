---
description: "Nell'API Copia Shadow del volume sono definiti i tipi di dati seguenti:"
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipi di dati dell'API Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b159156c4a892ae7ad07a4d988bb8f32b0f5689a440fe3f31da3d6c15470675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590563"
---
# <a name="volume-shadow-copy-api-data-types"></a>Tipi di dati dell'API Copia Shadow del volume

Nell'API Copia Shadow del volume sono definiti i tipi di dati seguenti:

<dl> <dt>

<span id="VSS_ID"></span><span id="vss_id"></span>VSS \_ ID
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

La **definizione \_ dell'ID VSS** specifica il formato dell'identificatore VSS generale. **\_ L'ID VSS** è un tipo di dati GUID standard.

**VSS \_ Gli ID** vengono usati per identificare gli elementi seguenti: copie shadow, set di copie shadow, provider, versioni del provider, writer (identificatore di classe del writer) e istanze di writer.

</dd> <dt>

<span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS \_ PWSZ
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

La **definizione \_ PWSZ di VSS** specifica una stringa di caratteri wide con terminazione Null (wchar).

</dd> <dt>

<span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>TIMESTAMP DI VSS \_
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

La definizione TIMESTAMP di **VSS \_** contiene le informazioni sul timestamp come valore intero a 64 bit contenente il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC). Questa definizione è intercambiabile con la [**struttura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

 

 
