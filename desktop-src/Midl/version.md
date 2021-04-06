---
title: version (attributo)
description: L'attributo \ Version \ Interface identifica una particolare versione tra più versioni di un'interfaccia RPC. Con l'attributo Version è possibile garantire che solo le versioni compatibili del software client e server siano consentite per l'associazione.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- attributo Version MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045766"
---
# <a name="version-attribute"></a>version (attributo)

L'attributo **\[ version \]** Interface identifica una particolare versione tra più versioni di un'interfaccia RPC. Con l'attributo Version è possibile garantire che solo le versioni compatibili del software client e server siano consentite per l'associazione.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*valore principale* 
</dt> <dd>

Specifica un Unsigned Integer breve compreso tra zero e 65.535, inclusi, che rappresenta il numero di versione principale.

</dd> <dt>

*valore secondario* 
</dt> <dd>

Specifica un Unsigned Integer breve compreso tra zero e 65.535, inclusi, che rappresenta il numero della versione secondaria. Il valore della versione secondaria è facoltativo. Se presente, il valore della versione secondaria è separato dal numero di versione principale per un carattere punto (.). Se non è specificato, il valore della versione secondaria è zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il compilatore MIDL non supporta più versioni di un'interfaccia COM. Di conseguenza, un elenco di attributi di interfaccia che include l'attributo dell' **\[** [**oggetto**](object.md) **\]** non può includere l'attributo **\[ version \]** . Per creare una nuova versione di un'interfaccia COM esistente, usare l'ereditarietà dell'interfaccia. Un'interfaccia COM derivata ha un UUID diverso ma eredita le funzioni membro di interfaccia, i codici di stato e gli attributi di interfaccia dell'interfaccia di base.

In combinazione con il **\[** [](uuid.md) **\]** valore UUID, il valore della **\[ versione \]** identifica in modo univoco l'interfaccia. La libreria di run-time passa i valori di **\[ versione \]** e **\[ UUID \]** al server quando il client chiama una funzione remota. Un client può eseguire l'associazione a un server per una data interfaccia se:

-   Il valore **\[ UUID \]** è lo stesso.
-   Il numero di versione principale è lo stesso.
-   Il numero di versione secondario del client è minore o uguale al numero di versione secondario del server.

Si tratta del vantaggio e del vantaggio degli utenti per mantenere la compatibilità verso l'alto tra versionsÂ, per modificare l'interfaccia in modo che solo il numero di versione secondario venga modificato. È possibile mantenere la compatibilità con l'alto quando si aggiungono nuovi tipi di dati che non vengono utilizzati dalle funzioni esistenti e quando si aggiungono nuove funzioni senza modificare la specifica dell'interfaccia per le funzioni esistenti.

Modificare il numero di versione principale se si verifica una delle condizioni seguenti:

-   Se si modifica un tipo di dati utilizzato da una funzione esistente.
-   Se si modifica la specifica dell'interfaccia per una funzione esistente (ad esempio l'aggiunta o la rimozione di un parametro).
-   Se si aggiungono callback chiamati da funzioni esistenti.

Modificare il numero di versione secondario se si verificano tutte le condizioni seguenti:

-   Se si aggiungono le definizioni o le costanti di tipo non utilizzate da funzioni o callback esistenti.
-   Se non si modificano funzioni esistenti e si aggiungono nuove funzioni all'interfaccia.
-   Se si aggiungono callback che non vengono chiamati da funzioni esistenti e i nuovi callback seguono tutte le funzioni esistenti.

Se le modifiche sono qualificate come una modifica compatibile con le versioni successive dell'interfaccia, attenersi alla procedura riportata di seguito.

**Per modificare il file dell'interfaccia (IDL)**

1.  Aggiungere nuove definizioni di costanti e tipi al file di interfaccia.
2.  Aggiungere funzioni di callback alla fine del file di interfaccia.
3.  Aggiungere nuove funzioni alla fine del file di interfaccia.

L'attributo **\[ version \]** può essere presente al massimo una volta nell'intestazione Interface.

Quando l'attributo Version non è presente, l'interfaccia ha la versione predefinita 0,0.

Il carattere punto tra i numeri principali e secondari è un delimitatore e non rappresenta un separatore decimale. Il numero secondario viene considerato come un numero intero. Gli zeri iniziali non sono significativi. Gli zeri finali sono significativi.

Ad esempio, l'impostazione della versione 1,11 rappresenta un valore principale di uno e un valore secondario pari a undici. La versione 1,11 non rappresenta un valore compreso tra 1,1 e 1,2.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[**oggetto**](object.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 




