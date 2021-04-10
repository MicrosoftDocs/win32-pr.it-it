---
description: Set di proprietà di trasporto dispositivo esterno
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Set di proprietà di trasporto dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125601"
---
# <a name="external-device-transport-property-set"></a>Set di proprietà di trasporto dispositivo esterno

Questo set di proprietà controlla il trasporto di dati da e verso un dispositivo esterno. Nella maggior parte dei casi, le applicazioni non devono utilizzare direttamente questo set di proprietà. Usare invece l'interfaccia [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .

Nella tabella seguente sono elencate le proprietà rilevanti per le applicazioni in modalità utente. Per una descrizione completa di questo set di proprietà, vedere Microsoft Windows Driver Development Kit DDK.



|                   |                           |
|-------------------|---------------------------|
| GUID set di proprietà | \_trasporto PROPSETID ext \_ |



 



| ID proprietà                                                                           | Descrizione                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**\_ricerca KSPROPERTY EXTXPORT \_ ATN \_**](ksproperty-extxport-atn-search.md)           | Cerca un numero di traccia assoluto (ATN). |
| [**KSPROPERTY \_ EXTXPORT \_ - \_ ricerca timecode**](ksproperty-extxport-timecode-search.md) | Cerca un codice temporale.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 



