---
description: Impostazione delle proprietà di acquisizione audio
ms.assetid: 81400072-91d7-4db4-86d3-d072663e691f
title: Impostazione delle proprietà di acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31afe61d4641906391934bafe4c3acb8a911a9fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225297"
---
# <a name="setting-audio-capture-properties"></a>Impostazione delle proprietà di acquisizione audio

Ogni pin di input nel filtro di acquisizione audio espone l'interfaccia [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) . Usare questa interfaccia per abilitare o disabilitare un input specifico, chiamando il metodo di [**\_ Abilitazione IAMAudioInputMixer::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamaudioinputmixer-put_enable) sul pin. Usare inoltre questa interfaccia per impostare le proprietà di un input, ad esempio i livelli Bass, Treble e volume. Se si acquisiscono più input contemporaneamente, è possibile controllare i livelli generale di Bassi, acuti e volumi tramite l'interfaccia **IAMAudioInputMixer** sul filtro stesso.

Le frequenze di campionamento e i formati audio disponibili per l'acquisizione sono determinati dal driver. Usare l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) sul pin di output del filtro di acquisizione audio per enumerare i formati e le frequenze di campionamento disponibili e impostare il formato desiderato. Il filtro può connettersi a valle a qualsiasi filtro che accetti il tipo di supporto del PIN di output.

Il filtro di acquisizione audio espone anche l'interfaccia [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) . Questa interfaccia è utile per controllare la quantità di latenza nell'anteprima audio. Per impostazione predefinita, il filtro di acquisizione audio utilizza una dimensione del buffer di mezzo secondo. Questa dimensione del buffer è ottimale per l'acquisizione, ma provoca un ritardo di anteprima di mezzo secondo. Per ridurre la latenza, chiamare il metodo [**IAMBufferNegotiation:: SuggestAllocatorProperties**](/windows/desktop/api/Strmif/nf-strmif-iambuffernegotiation-suggestallocatorproperties) prima di connettere il pin di output del filtro di acquisizione audio. Questo metodo accetta un puntatore alla struttura [**delle \_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) . Usare il membro **cbBuffer** per specificare la dimensione del buffer in byte. Un buffer di 80 millisecondi è generalmente sicuro, ma i buffer di 30 o 40 millisecondi potrebbero essere sufficienti. Se i buffer sono troppo piccoli, la qualità del suono sarà degradata.

 

 



