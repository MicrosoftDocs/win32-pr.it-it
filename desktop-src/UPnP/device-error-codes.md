---
title: Codici di errore del dispositivo
description: I Metodi InvokeAction e QueryStateVariable restituiscono valori HRESULT che potrebbero indicare un errore del dispositivo, ovvero un errore ricevuto da un dispositivo certificato UPnP.
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474542"
---
# <a name="device-error-codes"></a>Codici di errore del dispositivo

I metodi [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) restituiscono valori **HRESULT** che potrebbero indicare un errore del dispositivo, ovvero un errore ricevuto da un dispositivo certificato UPnP. Se viene ricevuto un errore da un dispositivo, il metodo ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) o [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) restituisce un valore **HRESULT** basato sul codice di errore del dispositivo, come illustrato in questo argomento. Poiché una conversione viene applicata al codice di errore del dispositivo per produrre un valore **HRESULT** , non è possibile leggere il codice di errore del dispositivo direttamente dal valore **HRESULT** .

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a>Conversione di un codice di errore del dispositivo in un HRESULT

Sono presenti codici di errore del dispositivo standard e non standard. I codici standard hanno lo stesso significato in tutti i dispositivi certificati UPnP e hanno valori minori di 600. I codici non standard sono specifici del fornitore e hanno valori compresi tra 600 e 899.

Indica se il codice di errore del dispositivo è standard determina il modo in cui viene generato il valore **HRESULT** :

-   Viene eseguito il mapping di un codice di errore standard del dispositivo a un valore **HRESULT** .

<!-- -->

-   Un codice di errore non standard del dispositivo è incorporato nel valore **HRESULT** applicando una formula.

Entrambe queste procedure possono essere invertite per determinare il codice di errore del dispositivo da un particolare valore **HRESULT** .

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a>Derivazione di un codice di errore del dispositivo da un valore HRESULT

Se il valore **HRESULT** è maggiore o uguale a **UPnP e \_ \_ Action \_ specific \_ base** (0x80040300) e minore o uguale a UPnP e **\_ \_ Action \_ specific \_ Max** (0x8004042B), il codice di errore del dispositivo non è conforme allo standard, utilizzare la formula nella sezione seguente per determinare il codice di errore. In caso contrario, il codice di errore del dispositivo è standard: usare la tabella nella sezione mapping per i codici di errore del dispositivo standard, che fornisce il mapping tra il valore **HRESULT** e il codice di errore del dispositivo.

Per una descrizione di testo dell'errore dopo una chiamata a [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), impostare il parametro *pvarRetVal* su una matrice vuota. Al ritorno, questo parametro conterrà una descrizione di testo dell'errore, se si verifica un errore.

### <a name="formula-for-nonstandard-device-error-codes"></a>Formula per i codici di errore del dispositivo non standard

Utilizzare la formula seguente se **l' \_ azione UPnP e la \_ \_ \_ base specifica dell'azione** ≤ **HRESULT** ≤ valore **\_ \_ \_ \_ massimo specifico per l'azione UPnP e**.

Codice di errore del dispositivo= (  -  **\_ \_ \_ \_ base specifica dell'azione E dell'azione** HRESULT) + **\_ \_ \_ base specifica dell'azione di errore**

Sostituendo i valori numerici effettivi, l'equazione è: codice errore dispositivo = (**HRESULT** -0x80040300) + 0x0258

### <a name="mapping-for-standard-device-error-codes"></a>Mapping per i codici di errore standard del dispositivo

Usare il mapping seguente se si  <  **specifica \_ una \_ \_ \_ base specifica dell'azione HRESULT UPnP E**.



| Valore HRESULT                    | Codice di errore del dispositivo                | Valore effettivo |
|----------------------------------|----------------------------------|--------------|
| \_azione UPnP E \_ non valida \_         | ERRORE \_ azione non valida \_           | 401          |
| \_argomenti UPnP E \_ non validi \_      | ERRORE \_ arg non valido \_              | 402          |
| UPNP \_ E \_ non \_ \_ sincronizzati           | ERRORE \_ \_ numero di sequenza non valido \_ | 403          |
| UPNP \_ E \_ variabile non valida \_       | variabile di errore \_ non valida \_         | 404          |
| \_richiesta di azione UPnP E \_ \_ \_ non riuscita | \_ \_ errore interno del dispositivo di errore \_   | 501          |



 

## <a name="more-information"></a>Altre informazioni

I codici di errore del dispositivo sono specificati nella [versione 1,0 dell'architettura del dispositivo UPnP](https://openconnectivity.org/resources/documents.asp). Le costanti indicate in questo argomento sono definite nei file UPnP. h e UPnP. idl.

 

 




