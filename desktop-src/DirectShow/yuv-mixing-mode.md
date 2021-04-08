---
description: Modalità di combinazione YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modalità di combinazione YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884129"
---
# <a name="yuv-mixing-mode"></a>Modalità di combinazione YUV

Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.

A partire da Windows XP Service Pack 2, VMR supporta una modalità di combinazione denominata YUV mixing mode. Questa modalità è particolarmente utile per le applicazioni TV o DVD avanzate. Si tratta di una parte della potenza del mixer VMR per ottenere prestazioni migliori su hardware grafico di fascia bassa che usa una struttura di architettura di memoria unificata. La modalità di combinazione YUV è supportata sia in VMR-7 che in VMR-9.

**Vantaggi**

La modalità di combinazione YUV presenta diversi vantaggi relativi alle prestazioni di rendering rispetto alla modalità di combinazione RGB originale supportata da VMR:

-   Quando VMR è in modalità di combinazione YUV, tutte le operazioni di deinterlacciamento e composizione del flusso video vengono eseguite nello spazio dei colori YUV. Le superfici YUV richiedono in genere da 50% a 60% di larghezza di banda di memoria inferiore rispetto alle superfici RGB equivalenti.
-   Il deinterlacciamento e la composizione del flusso vengono eseguiti da una singola chiamata al driver Graphics. Il driver può usare le funzionalità di multitexturing dell'hardware grafico, con conseguente risparmio di larghezza di banda della memoria.

Sebbene qualsiasi applicazione video possa usare la modalità di combinazione YUV, è destinata principalmente a due tipi di applicazione di riproduzione video:

1.  Applicazioni TV che visualizzano le didascalie o il televideo chiuso.
2.  Le applicazioni DVD visualizzano i dati delle sottoimmagini DVD o i sottotitoli chiusi.

**Restrizioni**

Una serie di restrizioni viene applicata da VMR quando viene inserita in modalità di combinazione YUV:

-   Il flusso 0 (il flusso connesso al pin di input 0) può essere progressivo o interlacciato; tutti gli altri flussi devono essere progressivi.
-   GUID \_ null (modalità di trama) non consentito per il flusso 0.
-   \_Non è possibile usare DeinterlacePref Weave come modalità di fallback perché questo potrebbe impedire la creazione di un dispositivo di deinterlacciamento. La modalità di combinazione YUV richiede un dispositivo deinterlacciato anche se il video in arrivo non è interlacciato.
-   Non è possibile apportare modifiche al valore alfa planare associato a ogni flusso di input di VMR.
-   L'utente non può modificare l'ordine Z dei flussi video connessi. L'ordine Z predefinito viene ricavato dall'ordine del PIN.
-   La chiave di colore non è supportata.
-   Il pin di input 0 deve ricevere il flusso video.
-   Gli altri pin di input possono ricevere solo i dati del sottoflusso video, ad esempio l'immagine secondaria del DVD, i sottotitoli o il televideo.
-   Gli altri pin di input possono accettare solo formati YUV alfanumerici per pixel, ad esempio AYUV, AI44 e IA44.
-   Nessuno dei pin di input di VMR può accettare qualsiasi formato RGB.
-   Le immagini bitmap fornite dall'applicazione non possono più essere combinate con il video prima della presentazione sullo schermo.
-   I singoli flussi secondari non possono essere invertiti orizzontalmente o verticalmente usando le funzioni del mixer "output Rectangle" di VMR. Sono supportati il riposizionamento e il ridimensionamento del flusso "normale".
-   Il colore di sfondo di combinazione (specificato da [**IVMRMixerControl:: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) è ancora specificato nello spazio colore RGB, come in modalità di combinazione RGB.

**Configuration**

Le applicazioni devono configurare in modo esplicito VMR per sfruttare i vantaggi della modalità di combinazione YUV; la modalità di combinazione RGB originale rimane quella predefinita. Per abilitare la modalità di combinazione YUV in VMR-7, chiamare [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con il \_ flag MixerPref RenderTargetYUV. Questa chiamata deve essere eseguita prima della connessione di uno dei pin di input di VMR. Per abilitare la modalità di combinazione YUV in VMR-9, chiamare [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il \_ flag MixerPref9 RenderTargetYUV.

L'unico modo per determinare se VMR-7 supporta la nuova modalità di combinazione YUV è provare a impostare VMR in tale modalità. Se la chiamata ha esito positivo, è comunque possibile riportare il VMR in modalità di combinazione RGB, se necessario. Dopo aver impostato la modalità di combinazione YUV, il VMR può essere modificato di nuovo in modalità di combinazione RGB solo dopo la disconnessione di tutti i pin di input.

In modalità di combinazione YUV è possibile ridurre il carico sull'unità di elaborazione grafica (GPU) applicando i flag seguenti nel metodo **SetMixingPrefs** :



| Flag                                                                                 | Descrizione                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Passa a Bob deinterlacciamento.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | Decimare l'immagine di un fattore 2 orizzontalmente e verticalmente. |



 

È possibile aggiungere o rimuovere questi flag mentre è in esecuzione il grafico dei filtri; la modifica viene applicata quando il mixer VMR compone il frame video successivo. I flag non si escludono a vicenda. Queste impostazioni riducono la qualità dell'immagine, quindi in genere si applicano solo quando la qualità del video è meno importante, ad esempio se il video viene riprodotto in una piccola parte dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




