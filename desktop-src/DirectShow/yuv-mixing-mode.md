---
description: Modalità di combinazione YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modalità di combinazione YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c5345eb80576ad0371558bb60d0b6651221bd98d7830cb968f39c16330fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290751"
---
# <a name="yuv-mixing-mode"></a>Modalità di combinazione YUV

Questo argomento si applica Windows XP Service Pack 2 o versioni successive.

A partire Windows XP Service Pack 2, VMR supporta una modalità di combinazione denominata modalità di combinazione YUV. Questa modalità è particolarmente utile per applicazioni TV o DVD avanzate. Scambia parte della potenza del mixer VMR per ottenere prestazioni migliori su hardware grafico di fascia bassa che usa una progettazione dell'architettura di memoria unificata. La modalità di combinazione YUV è supportata sia in VMR-7 che in VMR-9.

**Vantaggi**

La modalità di combinazione YUV presenta diversi vantaggi relativi alle prestazioni di rendering rispetto alla modalità di combinazione RGB originale supportata dal VMR:

-   Quando la macchina virtuale è in modalità di combinazione YUV, tutte le operazioni di de-interlacciamento e composizione del flusso video vengono eseguite nello spazio colore YUV. Le superfici YUV richiedono in genere una larghezza di banda di memoria dal 50% al 60% inferiore rispetto alle superfici RGB equivalenti.
-   Il dinterlacing e la composizione del flusso vengono eseguiti da una singola chiamata al driver di grafica. Il driver può usare le funzionalità multi texturing dell'hardware grafico, con conseguente risparmio aggiuntivo della larghezza di banda della memoria.

Anche se qualsiasi applicazione video può usare la modalità di combinazione YUV, è destinata principalmente a due tipi di applicazione di riproduzione video:

1.  Applicazioni TV che visualizzano sottotitoli codificati o teletext.
2.  Le applicazioni DVD visualizzano i dati delle immagini secondarie dei DVD o i sottotitoli codificati.

**Restrizioni**

Il vmr applica una serie di restrizioni quando viene imposta in modalità di combinazione YUV:

-   Il flusso 0 (il flusso connesso al Pin di input 0) può essere progressivo o interlacciato; tutti gli altri flussi devono essere progressivi.
-   GUID \_ NULL (modalità di compatibilità) non consentito per il flusso 0.
-   Non è possibile usare DeinterlacePref Sottoteni come modalità di fallback perché ciò potrebbe impedire la creazione di un dispositivo \_ de-interlacciato. La modalità di combinazione YUV richiede un dispositivo Dinterlace anche se il video in ingresso non è interlacciato.
-   Non è possibile apportare modifiche al valore alfa planare associato a ogni flusso di input vmr.
-   L'utente non può modificare l'ordine Z dei flussi video connessi. L'ordine Z predefinito deriva dall'ordine dei pin.
-   La chiave dei colori non è supportata.
-   Il pin di input 0 deve ricevere il flusso video.
-   Gli altri pin di input possono ricevere solo dati di flusso secondario video, ad esempio immagini secondarie DVD, sottotitoli codificati o teletext.
-   Gli altri pin di input possono accettare solo formati YUV alfa per pixel, ad esempio AYUV, AI44 e IA44.
-   Nessuno dei pin di input della macchina virtuale può accettare qualsiasi formato RGB.
-   Le immagini bitmap fornite dall'applicazione non possono più essere combinate con il video prima della presentazione sul display.
-   I singoli flussi secondari non possono essere invertiti orizzontalmente o verticalmente usando le funzioni "rettangolo di output" del mixer della macchina virtuale. Il riposizionamento e il ridimensionamento del flusso "Normale" sono supportati.
-   Il colore di sfondo misto (specificato da [**IVMRMixerControl::SetBackgroundClr)**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)viene comunque specificato nello spazio colore RGB, proprio come nella modalità di combinazione RGB.

**Configuration**

Le applicazioni devono configurare in modo esplicito la macchina virtuale per sfruttare i vantaggi della modalità di combinazione YUV. la modalità di combinazione RGB originale rimane la modalità di combinazione predefinita. Per abilitare la modalità di combinazione YUV in VMR-7, chiamare [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con il flag MixerPref \_ RenderTargetYUV. Questa chiamata deve essere effettuata prima che uno dei pin di input della macchina virtuale sia connesso. Per abilitare la modalità di combinazione YUV in VMR-9, chiamare [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il flag MixerPref9 \_ RenderTargetYUV.

L'unico modo per determinare se VMR-7 supporta la nuova modalità di combinazione YUV è provare a impostare la VMR in tale modalità. Se la chiamata ha esito positivo, è comunque possibile impostare nuovamente la vmr in modalità di combinazione RGB, se necessario. Dopo l'impostazione in modalità di combinazione YUV, la macchina virtuale può essere nuovamente impostata sulla modalità di combinazione RGB solo dopo che tutti i pin di input sono stati disconnessi.

In modalità di combinazione YUV è possibile ridurre il carico sull'unità di elaborazione grafica (GPU) applicando i flag seguenti nel **metodo SetMixingPrefs:**



| Flag                                                                                 | Descrizione                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Passare a bob deinterlacing.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | Affiancare l'immagine di un fattore di 2 orizzontalmente e verticalmente. |



 

È possibile aggiungere o rimuovere questi flag durante l'esecuzione del grafico dei filtri. La modifica viene applicata quando il mixer VMR compone il fotogramma video successivo. I flag non si escludono a vicenda. Queste impostazioni riducono la qualità dell'immagine, quindi in genere vengono applicate solo quando la qualità del video è meno importante, ad esempio se il video viene riprodotto in una piccola parte dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




