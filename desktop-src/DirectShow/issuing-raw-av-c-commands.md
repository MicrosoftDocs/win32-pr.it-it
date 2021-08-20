---
description: Esecuzione di comandi AV/C non elaborati
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Esecuzione di comandi AV/C non elaborati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729cad0be3a55a3f95592e54e8f91b9074892a8d111da9ad996b4e00a136cbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153788"
---
# <a name="issuing-raw-avc-commands"></a>Esecuzione di comandi AV/C non elaborati

Le interfacce [**IAMExtDevice,**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice) [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funzionano traducendo le chiamate al metodo in comandi per il driver, quindi interpretando la risposta del driver e restituirla tramite **un HRESULT** o un parametro di output. Tuttavia, alcune funzioni del dispositivo potrebbero non essere accessibili tramite questi metodi. MsDV supporta quindi l'invio di comandi AV/C non elaborati al dispositivo.

Quando si usa questa funzionalità, tenere presente quanto segue:

-   Il comando viene passato direttamente al dispositivo, senza controllo degli errori o convalida dei parametri. Per questo motivo, è consigliabile eseguire comandi AV/C non elaborati solo quando le interfacce DirectShow non implementano la funzionalità necessaria.
-   Tutti i comandi AV/C non elaborati sono sincroni. Il thread che emette il comando si blocca fino alla fine del comando.
-   È possibile specificare un solo comando alla volta. Durante l'elaborazione del comando, il dispositivo rifiuterà eventuali comandi aggiuntivi.
-   Il driver UVC non supporta i comandi AV/C non elaborati.

Per inviare un comando AV/C, formattare il comando come matrice di byte. Chiamare quindi [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Passare il \_ flag ED RAW \_ EXT \_ DEV \_ CMD, le dimensioni della matrice e la matrice. È necessario eseguire il cast dell'indirizzo della matrice a **un tipo \* LPOLESTR,** perché lo scopo originale di questo parametro era restituire un valore stringa.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR*) AvcCmd);
```



Il contenuto della matrice viene passato direttamente al dispositivo, quindi è necessario prestare attenzione a formattarlo correttamente. Un comando può avere come destinazione l'unità (cinecorder) o una sottounità (nastro o fotocamera). Gli standard pertinenti sono disponibili nel sito Web [1394 Trade Association](https://1394ta.org).

-   Specifica generale del set di comandi dell'interfaccia digitale AV/C
-   AV/C Tape Recorder/Player Subunit Specification

Il primo descrive come formattare i comandi AV/C ed elenca i comandi di unità. La seconda specifica elenca i comandi delle sottounità.

Il **metodo GetTransportBasicParameters** può restituire uno dei codici di errore seguenti:



| Codice di errore              | Descrizione                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| TIMEOUT \_ ERRORE          | Timeout del comando.                                                           |
| ERRORE \_ REQ \_ NOT \_ ACCEP  | Il dispositivo non ha accettato il comando.                                           |
| ERRORE \_ NON \_ SUPPORTATO   | Il dispositivo non supporta il comando .                                         |
| RICHIESTA \_ DI \_ ERRORE INTERROTTA | Il comando è stato interrotto. Possbly the device was removed or a bus reset occurred. (Il dispositivo è stato rimosso o si è verificato un ripristino del bus. |



 

> [!Note]  
> Questi errori vengono restituiti come codici di errore Win32, non come HRESULT, pertanto è consigliabile verificare questi valori direttamente, anziché usare le macro **SUCCEEDED** **e FAILED.**

 

Se il metodo restituisce S \_ OK, la risposta dal dispositivo viene copiata nella matrice . Il payload della risposta potrebbe essere più grande del comando, pertanto è necessario allocare un buffer sufficientemente grande da contenerlo. La dimensione massima del payload è 512 byte. Si noti che il valore restituito S \_ OK non significa sempre che il dispositivo ha eseguito correttamente il comando. L'applicazione deve esaminare il payload della risposta per determinare lo stato.

L'esempio seguente mostra il comando per cercare una ricerca di numeri di traccia assoluti:


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

[Controllo di un videocamere DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



