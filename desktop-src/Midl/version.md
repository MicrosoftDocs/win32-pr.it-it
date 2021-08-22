---
title: version (attributo)
description: L'attributo dell'interfaccia \version\ identifica una versione specifica tra più versioni di un'interfaccia RPC. Con l'attributo version, si garantisce che solo le versioni compatibili del software client e server siano consentite per l'associazione.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- Attributo version MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c72cc825183740d856c20b9e5c76ece472f82db405d9560e6502f6e32985b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252111"
---
# <a name="version-attribute"></a>version (attributo)

**\[ L'attributo \]** dell'interfaccia della versione identifica una versione specifica tra più versioni di un'interfaccia RPC. Con l'attributo version, si garantisce che solo le versioni compatibili del software client e server siano consentite per l'associazione.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore principale* 
</dt> <dd>

Specifica un intero senza segno breve compreso tra zero e 65.535 inclusi che rappresenta il numero di versione principale.

</dd> <dt>

*minor-value* 
</dt> <dd>

Specifica un intero senza segno breve compreso tra zero e 65.535 inclusi che rappresenta il numero di versione secondaria. Il valore della versione secondaria è facoltativo. Se presente, il valore della versione secondaria è separato dal numero di versione principale da un carattere punto (.). Se non specificato, il valore della versione secondaria è zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il compilatore MIDL non supporta più versioni di un'interfaccia COM. Di conseguenza, un elenco di attributi di interfaccia che include **\[** [**l'attributo dell'oggetto**](object.md) **\]** non può includere l'attributo **\[ version. \]** Per creare una nuova versione di un'interfaccia COM esistente, usare l'ereditarietà dell'interfaccia. Un'interfaccia COM derivata ha un UUID diverso, ma eredita le funzioni membro dell'interfaccia, i codici di stato e gli attributi dell'interfaccia di base.

In combinazione con il valore **\[** [**uuid,**](uuid.md) **\]** il valore **\[ della \]** versione identifica in modo univoco l'interfaccia. La libreria di runtime passa la **\[ versione e \]** i valori **\[ uuid \]** al server quando il client chiama una funzione remota. Un client può eseguire l'associazione a un server per una determinata interfaccia se:

-   Il **\[ valore \] uuid** è lo stesso.
-   Il numero di versione principale è lo stesso.
-   Il numero di versione secondaria del client è minore o uguale al numero di versione secondaria del server.

È vantaggioso e vantaggio per gli utenti mantenere la compatibilità verso l'alto tra le versioni, ad esempio modificare l'interfaccia in modo che cambi solo il numero di versione secondaria. È possibile mantenere la compatibilità verso l'alto quando si aggiungono nuovi tipi di dati che non vengono usati dalle funzioni esistenti e quando si aggiungono nuove funzioni senza modificare la specifica dell'interfaccia per le funzioni esistenti.

Modificare il numero di versione principale se si verifica una delle condizioni seguenti:

-   Se si modifica un tipo di dati utilizzato da una funzione esistente.
-   Se si modifica la specifica dell'interfaccia per una funzione esistente, ad esempio aggiungendo o rimuovendo un parametro.
-   Se si aggiungono callback chiamati da funzioni esistenti.

Modificare il numero di versione secondaria se si applicano tutte le condizioni seguenti:

-   Se si aggiungono definizioni di tipo o costanti che non vengono usate da funzioni o callback esistenti.
-   Se non si modificano le funzioni esistenti e si aggiungono nuove funzioni all'interfaccia.
-   Se si aggiungono callback che non vengono chiamati da alcuna funzione esistente e i nuovi callback seguono le funzioni esistenti.

Se le modifiche si qualificano come una modifica verso l'alto compatibile con l'interfaccia, usare la procedura seguente.

**Per modificare il file di interfaccia (IDL)**

1.  Aggiungere nuove definizioni di costanti e tipi al file di interfaccia.
2.  Aggiungere funzioni di callback alla fine del file di interfaccia.
3.  Aggiungere nuove funzioni alla fine del file di interfaccia.

**\[ L'attributo version \]** può essere presente al massimo una volta nell'intestazione dell'interfaccia.

Quando l'attributo version non è presente, la versione predefinita dell'interfaccia è 0.0.

Il carattere punto tra i numeri principali e secondari è un delimitatore e non rappresenta un separatore decimale. Il numero secondario viene considerato come un numero intero. Gli zeri iniziali non sono significativi. Gli zeri finali sono significativi.

Ad esempio, l'impostazione della versione 1.11 rappresenta un valore principale pari a uno e un valore secondario pari a 11. La versione 1.11 non rappresenta un valore compreso tra 1.1 e 1.2.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Interfaccia**](interface.md)
</dt> <dt>

[**Oggetto**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 




