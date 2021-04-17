---
title: notifica attributo
description: L'attributo \ Notify \ indica al compilatore MIDL di generare una chiamata a una procedura \ Notify \ sul lato server dell'applicazione.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notifica attributo MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516213"
---
# <a name="notify-attribute"></a>notifica attributo

L'attributo **\[ Notify \]** indica al compilatore MIDL di generare una chiamata a una procedura **\[ Notify \]** sul lato server dell'applicazione.

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome procedura* 
</dt> <dd>

Nome della procedura remota a cui verrà associata la procedura di notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La procedura di **\[ notifica \]** chiamata come risultato dell'attributo **\[ Notify \]** è associata a una specifica procedura remota nel server. Si tratta di un concetto simile a una funzione di callback. Lo stub chiama la procedura **\[ Notify \]** dopo che sono stati sottoposti a marshalling tutti gli argomenti di output della procedura remota a cui è associato ed è stata liberata la memoria associata ai parametri. La routine **\[ Notify \]** viene chiamata se una chiamata ha esito negativo prima dell'esecuzione della routine del server. Se, ad esempio, si verifica un errore del server durante l'unmarshalling a causa della ricezione di dati non validi dal client, \[ \] viene chiamata la routine di notifica.

L'attributo **\[ Notify \]** è utile per lo sviluppo di applicazioni che acquisiscono risorse in procedure remote. Queste risorse vengono quindi liberate nella procedura di **\[ notifica \]** dopo il marshalling completo dei parametri di output della procedura remota.

Il nome della procedura di **\[ notifica \]** è il nome della procedura remota con suffisso **\_ notifica**. La procedura di **\_ notifica** non richiede alcun parametro e non restituisce alcun risultato. Nel file di intestazione viene anche generato un prototipo di questa procedura. Ad esempio, se il file IDL contiene quanto segue:

``` syntax
MyProcedure([in] short S);
```

Specificare quanto segue in ACF per MIDL per generare la chiamata di **\_ notifica** :

``` syntax
[notify] MyProcedure();
```

Il compilatore MIDL genererà il codice stub del server che contiene la chiamata seguente alla procedura **\_ Notify** :

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

 

 




