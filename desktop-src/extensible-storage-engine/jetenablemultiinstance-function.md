---
description: 'Altre informazioni su: funzione JetEnableMultiInstance'
title: JetEnableMultiInstance (funzione)
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319635"
---
# <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance (funzione)


_**Si applica a:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance (funzione)

La funzione **JetEnableMultiInstance** configura il motore di database per l'utilizzo con più istanze nello stesso processo. Una matrice facoltativa di parametri di sistema globale è disponibile per il primo chiamante che consente la modifica alla modalità a istanze diverse.

**Windows XP: JetEnableMultiInstance** è stato introdotto in Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parametri

*psetsysparam*

Matrice di parametri di sistema globale da impostare se e solo se il motore entra in modalità a istanze diverse in seguito a questa chiamata. Se *csetsysparam* è zero, *psetsysparam* viene ignorato.

*csetsysparam*

Il numero di elementi per la matrice di parametri globali da impostare se e solo se il motore entra in modalità a istanze diverse in seguito a questa chiamata. Se *csetsysparam* è zero, *psetsysparam* viene ignorato.

*pcsetsucceed*

Puntatore al numero di parametri di sistema globale configurati correttamente in seguito a questa chiamata.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il tipo di dati [JET_ERR](./jet-err.md) con uno dei seguenti codici restituiti. Per ulteriori informazioni sugli errori ESE possibili, vedere la pagina relativa agli errori e ai [parametri di gestione degli](./error-handling-parameters.md)errori del [motore di archiviazione estensibile](./extensible-storage-engine-errors.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Codice restituito</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Operazione riuscita.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>I parametri specificati per l'indice tupla non sono consentiti. Questo errore può essere restituito da <strong>JetEnableMultiInstance</strong> solo quando si imposta <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> su un valore non valido.</p>
<p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Il percorso di file system specificato non è valido. Questo errore può essere restituito da <strong>JetEnableMultiInstance</strong> solo quando si impostano parametri di sistema che rappresentano file System percorsi. Ad esempio, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> possibile restituire l'errore.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>L'operazione non è riuscita perché non è valida quando il motore di database funziona in modalità a istanza singola (modalità di compatibilità di Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemParamsAlreadySet</p></td>
<td><p><strong>JetEnableMultiInstance</strong> non riuscito perché il motore è già in modalità a istanze diverse.</p>
<p><strong>Nota  </strong> Questa operazione si verificherà anche se non viene specificato alcun parametro di sistema.</p></td>
</tr>
</tbody>
</table>


Se questa funzione ha esito positivo, il motore di database verrà configurato per l'esecuzione in modalità a istanze diverse. Anche il motore è stato configurato correttamente con l'elenco facoltativo di parametri di sistema globali.

Se questa funzione ha esito negativo, il motore di database rimarrà nella modalità corrente. Se *pcsetsucceed* è diverso da zero, il numero di parametri di sistema rimarrà impostato.

#### <a name="remarks"></a>Commenti

Questa funzione deve essere utilizzata solo se l'applicazione deve configurare un determinato set di parametri di sistema in modo atomico quando si configura il motore di database per l'utilizzo in uno scenario multiutente nello stesso processo. Se è disponibile un altro metodo di sincronizzazione, è preferibile chiamare [JetCreateInstance](./jetcreateinstance-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) separatamente.

#### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Libreria</strong></p></td>
<td><p>Usare ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Richiede ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JetEnableMultiInstanceW</strong> (Unicode) e <strong>JetEnableMultiInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
