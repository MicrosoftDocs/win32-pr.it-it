---
description: Questa sezione descrive come scrivere una trasformazione Media Foundation personalizzata (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Scrittura di un MFT personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471657"
---
# <a name="writing-a-custom-mft"></a>Scrittura di un MFT personalizzato

Questa sezione descrive come scrivere una trasformazione Media Foundation personalizzata (MFT).

## <a name="mft-checklist"></a>Elenco di controllo MFT

Quando si implementa un MFT personalizzato, usare l'elenco di controllo seguente per determinare i requisiti:




| | | Tutti i MFT | Tutti i MFT devono implementare <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.<br /> Gli argomenti seguenti forniscono altre informazioni sull'implementazione di questa interfaccia:<ul><li><a href="basic-mft-processing-model.md">Modello di elaborazione MFT di base</a></li><li><a href="time-stamps-and-durations.md">Timestamp e durate</a></li><li><a href="handling-stream-changes.md">Gestione delle modifiche del flusso</a></li></ul><br /> | | Codificatori e decodificatori | Requisiti: vedere <a href="implementing-a-codec-mft.md">Implementazione di un codec MFT</a>.<br /> Consigliato: <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>implementare IMFQualityAdvise</strong></a> o <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>per supportare le notifiche di qualità del servizio (QoS).<br /> | | Decodificatori video e processori video | Facoltativo: supporta l'accelerazione video DirectX.<br /><ul><li><a href="direct3d-aware-mfts.md">MFT in grado di riconoscere Direct3D</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">Supporto di DXVA 2.0 in Media Foundation</a></li></ul> | | Codec hardware | Vedere <a href="hardware-mfts.md">MFT hardware</a>. | | Per rendere l'MFT individuabile dalle applicazioni... | Vedere <a href="registering-and-enumerating-mfts.md">Registrazione ed enumerazione di MFT</a>. | | Elaborazione dati asincrona | Il modello MFT predefinito usa chiamate sincrone (bloccante) per elaborare i dati. Per alcuni MFT, l'elaborazione asincrona può essere più efficiente. Tuttavia, è anche più complesso da implementare.<br /> Per altre informazioni, vedere <a href="asynchronous-mfts.md">MFT asincroni</a>.<br /> | | Controllo della frequenza, modalità trick o riproduzione inversa | Vedere <a href="implementing-rate-control.md">Implementazione del controllo frequenza</a>. | | Se MFT crea thread | Implementare <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>l'interfaccia IMFRealTimeClient.</strong></a> | | Se mFT ha restrizioni di licenza... | È consigliabile usare il meccanismo field-of-use. Vedere <a href="field-of-use-restrictions.md">Restrizioni relative al campo di utilizzo</a>. | | Se si sta trasando un oggetto DirectX Media Object (DMO)... | Vedere <a href="comparison-of-mfts-and-dmos.md">Confronto tra MFT e DMO.</a> | 




 

Questa sezione contiene i seguenti argomenti:

-   [Timestamp e durate](time-stamps-and-durations.md)
-   [Gestione delle modifiche del flusso](handling-stream-changes.md)
-   [Implementazione di un codec MFT](implementing-a-codec-mft.md)
-   [MFT in grado di riconoscere Direct3D](direct3d-aware-mfts.md)
-   [MFT hardware](hardware-mfts.md)
-   [Merito dei codec](codec-merit.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> </dl>

 

 




