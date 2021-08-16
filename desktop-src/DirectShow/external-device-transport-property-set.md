---
description: Set di proprietà Trasporto dispositivo esterno
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Set di proprietà Trasporto dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef7db31dfe80fae0178aa329ce7e3c6cd55d3a6acbef7fd5a8ccda07943bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685671"
---
# <a name="external-device-transport-property-set"></a>Set di proprietà Trasporto dispositivo esterno

Questo set di proprietà controlla il trasporto dei dati da e verso un dispositivo esterno. Nella maggior parte dei casi, le applicazioni non devono usare direttamente questa proprietà impostata. Usare invece [**l'interfaccia IAMExtTransport.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)

Nella tabella seguente sono elencate le proprietà rilevanti per le applicazioni in modalità utente. Per una descrizione completa di questo set di proprietà, vedere microsoft Windows Driver Development Kit DDK.



| Etichetta | Valore |
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

 

 



