---
description: Emissione di comandi AV/C non elaborati
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emissione di comandi AV/C non elaborati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401155"
---
# <a name="issuing-raw-avc-commands"></a>Emissione di comandi AV/C non elaborati

Le interfacce [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funzionano traducendo le chiamate al metodo in comandi per il driver, interpretando quindi la risposta del driver e restituendo il valore tramite un **HRESULT** o un parametro di output. Tuttavia, alcune funzioni del dispositivo potrebbero non essere accessibili tramite questi metodi. MSDV supporta quindi l'invio di comandi AV/C non elaborati al dispositivo.

Quando si usa questa funzionalità, è necessario tenere presente quanto segue:

-   Il comando viene passato direttamente al dispositivo, senza il controllo degli errori o la convalida dei parametri. Per questo motivo, è necessario emettere comandi AV/C non elaborati solo quando le interfacce DirectShow non implementano la funzionalità necessaria.
-   Tutti i comandi AV/C non elaborati sono sincroni. Il thread che emette il comando si blocca fino a quando il comando non restituisce.
-   È possibile assegnare un solo comando alla volta. Durante l'elaborazione del comando, il dispositivo rifiuterà qualsiasi comando aggiuntivo.
-   Il driver UVC non supporta i comandi AV/C non elaborati.

Per inviare un comando AV/C, formattare il comando come una matrice di byte. Quindi, chiamare [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Passare il flag ED \_ \_ ext \_ dev \_ , le dimensioni della matrice e la matrice. È necessario eseguire il cast dell'indirizzo della matrice a un tipo **LPOLESTR \** _, perché lo scopo originale di questo parametro è restituire un valore stringa.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



Il contenuto della matrice viene passato direttamente al dispositivo, quindi è necessario prestare attenzione a formattarlo correttamente. Un comando può avere come destinazione l'unità (videocamera) o un'unità secondaria (nastro o fotocamera). Gli standard pertinenti sono disponibili nel [sito Web di associazione commerciale 1394](https://1394ta.org).

-   Specifica generale del set di comandi dell'interfaccia digitale AV/C
-   Specifica di unità di registrazione/lettore nastri AV/C

Il primo descrive come formattare i comandi AV/C ed elenca i comandi di unità. La seconda specifica elenca i comandi delle sottounità.

Il metodo **GetTransportBasicParameters** può restituire uno dei codici di errore seguenti:



| Codice di errore              | Descrizione                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| \_timeout errore          | Timeout del comando.                                                           |
| ERRORE \_ req \_ non \_ definit  | Il dispositivo non ha accettato il comando.                                           |
| ERRORE \_ non \_ supportato   | Il dispositivo non supporta il comando.                                         |
| richiesta di errore \_ \_ interrotta | Il comando è stato interrotto. Possbly il dispositivo è stato rimosso o si è verificata una reimpostazione del bus. |



 

> [!Note]  
> Questi errori vengono restituiti come codici di errore Win32, non HRESULT, quindi è consigliabile eseguire il test direttamente di questi valori, anziché utilizzare le macro **succeeded** e **failed** .

 

Se il metodo restituisce S \_ OK, la risposta dal dispositivo viene copiata nella matrice. Il payload della risposta potrebbe essere più grande del comando, quindi è necessario allocare un buffer sufficientemente grande da contenerlo. Le dimensioni massime del payload sono pari a 512 byte. Si noti che un valore restituito di S \_ OK non sempre significa che il dispositivo ha eseguito correttamente il comando. Per determinare lo stato, l'applicazione deve esaminare il payload della risposta.

Nell'esempio seguente viene illustrato il comando per cercare una ricerca di un numero di traccia assoluto:


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



