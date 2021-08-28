---
description: Altre informazioni sulla funzione JetEnableMultiInstance
title: Funzione JetEnableMultiInstance
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
ms.openlocfilehash: dba0b8094187f3a59f05f4b1a1fae1b95dbab66e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989034"
---
# <a name="jetenablemultiinstance-function"></a>Funzione JetEnableMultiInstance


_**Si applica a:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>Funzione JetEnableMultiInstance

La **funzione JetEnableMultiInstance** configura il motore di database per l'uso con più istanze nello stesso processo. Una matrice facoltativa di parametri di sistema globali è disponibile per il primo chiamante consentendo la modifica alla modalità a più istanze.

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

Matrice di parametri di sistema globali da impostare se e solo se il motore entra in modalità a più istanze come risultato di questa chiamata. Se *csetsysparam* è zero, *psetsysparam viene* ignorato.

*csetsysparam*

Numero di elementi per la matrice di parametri globali da impostare se e solo se il motore entra in modalità a più istanze come risultato di questa chiamata. Se *csetsysparam* è zero, *psetsysparam viene* ignorato.

*pcsetsucceed*

Puntatore al conteggio dei parametri di sistema globali configurati correttamente come risultato di questa chiamata.

### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere Errori del [motore di Archiviazione](./extensible-storage-engine-errors.md) estendibile e Parametri di gestione degli [errori](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>I parametri dell'indice di tupla specificati non sono consentiti. Questo errore può essere restituito <strong>da JetEnableMultiInstance</strong> solo quando si imposta JET_paramIndexTuplesLengthMin <a href="gg294119(v=exchg.10).md">,</a> <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> su un valore non valido.</p><p><strong>Windows XP:</strong>  Questo valore restituito è stato introdotto in Windows XP.</p> | 
| <p>JET_errInvalidPath</p> | <p>Il percorso file system specificato non è valido. Questo errore può essere restituito <strong>da JetEnableMultiInstance</strong> solo quando si impostano parametri di sistema che rappresentano file system percorsi. Ad esempio, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> può restituire questo errore.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>L'operazione non è riuscita perché non è valida quando il motore di database funziona in modalità a istanza singola (Windows modalità di compatibilità 2000).</p> | 
| <p>JET_errSystemParamsAlreadySet</p> | <p><strong>JetEnableMultiInstance</strong> non riuscito perché il motore è già in modalità a istanze multipla.</p><p><strong>Nota  </strong> Ciò si verifica anche se non viene specificato alcun parametro di sistema.</p> | 



Se questa funzione ha esito positivo, il motore di database verrà configurato per l'esecuzione in modalità a più istanze. Il motore è stato anche configurato correttamente con l'elenco facoltativo di parametri di sistema globali.

Se questa funzione ha esito negativo, il motore di database rimarrà in modalità corrente. Se *pcsetsucceed* è diverso da zero, il numero di parametri di sistema rimarrà impostato.

#### <a name="remarks"></a>Commenti

Questa funzione deve essere usata solo se l'applicazione deve configurare un determinato set di parametri di sistema in modo atomico quando si configura il motore di database per l'uso in uno scenario multi-utente nello stesso processo. Se è disponibile un altro metodo di sincronizzazione, è preferibile chiamare [separatamente JetCreateInstance](./jetcreateinstance-function.md) [e JetSetSystemParameter.](./jetsetsystemparameter-function.md)

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista o Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008 o Windows Server 2003.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetEnableMultiInstanceW</strong> (Unicode) e <strong>JetEnableMultiInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
