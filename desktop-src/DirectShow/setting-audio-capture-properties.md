---
description: Impostazione delle proprietà di acquisizione audio
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Impostazione delle proprietà di acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0230f3a9679871380f6eecf09ad5589bfc02c13e0d1433bab8e3b4075de2cf5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078811"
---
# <a name="setting-audio-capture-properties"></a>Impostazione delle proprietà di acquisizione audio

Ogni pin di input nel filtro di acquisizione audio espone [**l'interfaccia IAMAudioInputMixer.**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) Usare questa interfaccia per abilitare o disabilitare un input specifico chiamando il metodo [**IAMAudioInputMixer::p ut \_ Enable**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) sul pin. Usare anche questa interfaccia per impostare le proprietà di un input, ad esempio i livelli basso, acuto e volume. Se si acquisisce più input contemporaneamente, è possibile controllare i livelli complessivi di bassi, alti e volumi tramite l'interfaccia **IAMAudioInputMixer** sul filtro stesso.

Le frequenze di campionamento disponibili e i formati audio per l'acquisizione sono determinati dal driver. Usare [**l'interfaccia IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sul pin di output del filtro di acquisizione audio per enumerare le frequenze e i formati di campionamento disponibili e impostare il formato desiderato. Il filtro può connettersi a valle a qualsiasi filtro che accetta il tipo di supporto del pin di output.

Il filtro di acquisizione audio espone anche [**l'interfaccia IAMBufferNegotiation.**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) Questa interfaccia è utile per controllare la quantità di latenza nell'anteprima audio. Per impostazione predefinita, il filtro Acquisizione audio usa una dimensione del buffer di mezzo secondo. Questa dimensione del buffer è ottimale per l'acquisizione, ma causa un ritardo di mezzo secondo in anteprima. Per ridurre la latenza, chiamare il metodo [**IAMBufferNegotiation::SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) prima di connettere il pin di output del filtro di acquisizione audio. Questo metodo accetta un puntatore alla struttura [**ALLOCATOR \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Usare il **membro cbBuffer** per specificare le dimensioni del buffer, in byte. Un buffer di 80 millisecondi è generalmente sicuro, ma potrebbero essere sufficienti buffer di 30 o 40 millisecondi. Se i buffer sono troppo piccoli, la qualità del suono sarà ridotta.

 

 



