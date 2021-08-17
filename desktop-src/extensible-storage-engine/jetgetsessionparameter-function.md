---
description: Altre informazioni sulla funzione JetGetSessionParameter
title: Funzione JetGetSessionParameter
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: effd1ea5a9489df0a85af54a79cd773cc05b2fa3d6dbe57096a61fbd4c79c25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472031"
---
# <a name="jetgetsessionparameter-function"></a>Funzione JetGetSessionParameter


_**Si applica a:** Windows | Windows Server_

La **funzione JetGetSessionParameter** legge il parametro di sessione per la sessione specificata.

La **funzione JetGetSessionParameter** è stata introdotta nel Windows 8 operativo.

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>Parametri

*sesid*

Sessione da utilizzare per questa chiamata.

Se specificato, l'istanza specificata viene ignorata e verrà usata l'istanza associata alla sessione.

*sesparamid*

ID del parametro di sessione da impostare.

*pvParam*

Dati in questo parametro di sessione.

*cbParamMax*

Dimensione massima del set di dati in questo parametro di sessione.

*pcbParamActual*

Dimensioni effettive del set di dati in questo parametro di sessione.

### <a name="return-value"></a>Valore restituito

In caso di esito positivo, il buffer di output appropriato per il parametro di sessione richiesto verrà impostato sul valore di tale parametro di sessione.

In caso di errore, lo stato dei buffer di output non sarà definito.

#### <a name="remarks"></a>Commenti

Il parametro session viene usato per la durata della sessione o fino a quando il valore non viene reimpostato.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedi anche

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parametri di sistema](./extensible-storage-engine-system-parameters.md)
