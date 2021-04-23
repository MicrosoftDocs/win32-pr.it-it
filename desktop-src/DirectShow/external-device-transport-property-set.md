---
description: Set di proprietà Trasporto dispositivo esterno
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Set di proprietà Trasporto dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909219"
---
# <a name="external-device-transport-property-set"></a>Set di proprietà Trasporto dispositivo esterno

Questo set di proprietà controlla il trasporto dei dati da e verso un dispositivo esterno. Nella maggior parte dei casi, le applicazioni non devono usare direttamente questa proprietà impostata. Usare invece [**l'interfaccia IAMExtTransport.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)

Nella tabella seguente sono elencate le proprietà rilevanti per le applicazioni in modalità utente. Per una descrizione completa di questo set di proprietà, vedere microsoft Windows Driver Development Kit DDK.



| Label | Valore |
|-------------------|---------------------------|
| GUID set di proprietà | PROPSETID \_ EXT \_ TRANSPORT |



 



| ID proprietà                                                                           | Descrizione                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**](ksproperty-extxport-atn-search.md)           | Cerca un numero di traccia assoluto (ATN). |
| [**KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH**](ksproperty-extxport-timecode-search.md) | Cerca un time code.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 



