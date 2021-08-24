---
title: Attributo notify
description: L'attributo \ notify\ indica al compilatore MIDL di generare una chiamata a una procedura \ notify\ sul lato server dell'applicazione.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- attributo notify MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf1bb1c4f522cecb5fe81a317267e2cffff2da638e3a8c09a412ae8d94a149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066861"
---
# <a name="notify-attribute"></a>Attributo notify

**\[ L'attributo \] notify** indica al compilatore MIDL di generare una chiamata a una procedura **\[ di \]** notifica sul lato server dell'applicazione.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*procedure-name* 
</dt> <dd>

Nome della procedura remota a cui verrà associata la procedura di notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\[ procedura di \]** notifica chiamata come risultato dell'attributo **\[ notify \]** è associata a una particolare procedura remota nel server. Si tratta di un concetto simile a una funzione di callback. Lo stub chiama la **\[ routine notify \]** dopo che tutti gli argomenti di output della procedura remota a cui è associata sono stati sottoposti a marshalling e la memoria associata ai parametri viene liberata. La **\[ routine notify \]** viene chiamata se una chiamata non riesce prima dell'esecuzione della routine del server. Ad esempio, se un server ha esito negativo durante l'unmarshaling a causa della ricezione di dati non validi dal client, viene chiamata la \[ \] routine di notifica.

**\[ L'attributo notify \]** è utile per sviluppare applicazioni che acquisisce risorse in procedure remote. Queste risorse vengono quindi liberate nella **\[ procedura di \]** notifica dopo il marshalling completo dei parametri di output della procedura remota.

Il **\[ nome della \]** procedura di notifica è il nome della procedura remota con suffisso **\_ notify**. La **\_ procedura notify** non richiede parametri e non restituisce un risultato. Nel file di intestazione viene generato anche un prototipo di questa procedura. Ad esempio, se il file IDL contiene quanto segue:

``` syntax
MyProcedure([in] short S);
```

Specificare quanto segue in ACF per MIDL per generare la **\_ chiamata di** notifica:

``` syntax
[notify] MyProcedure();
```

Il compilatore MIDL genererà codice stub del server che contiene la chiamata seguente alla **\_ procedura di** notifica:

``` syntax
MyProcedure_notify();
```

Il file di intestazione conterrà un prototipo:

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a>Esempi

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> </dl>

 

 




