---
description: In questa sezione viene descritto come scrivere una trasformazione Media Foundation personalizzata (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Scrittura di un MFT personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882214"
---
# <a name="writing-a-custom-mft"></a>Scrittura di un MFT personalizzato

In questa sezione viene descritto come scrivere una trasformazione Media Foundation personalizzata (MFT).

## <a name="mft-checklist"></a>Elenco di controllo MFT

Quando si implementa un MFT personalizzato, utilizzare l'elenco di controllo seguente per determinare i requisiti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tutte le MFTs</td>
<td>Tutti MFTs devono implementare <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.<br/> Negli argomenti seguenti vengono fornite ulteriori informazioni sull'implementazione di questa interfaccia:
<ul>
<li><a href="basic-mft-processing-model.md">Modello di elaborazione MFT di base</a></li>
<li><a href="time-stamps-and-durations.md">Timestamp e durate</a></li>
<li><a href="handling-stream-changes.md">Gestione delle modifiche dei flussi</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Codificatori e decodificatori</td>
<td>Requisiti: vedere <a href="implementing-a-codec-mft.md">implementazione di un codec MFT</a>.<br/> Consigliato: implementare <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> o <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>per supportare le notifiche di qualità del servizio (QoS).<br/></td>
</tr>
<tr class="odd">
<td>Decodificatori video e processori video</td>
<td>Facoltativo: supporta l'accelerazione video DirectX.<br/>
<ul>
<li><a href="direct3d-aware-mfts.md">MFTs compatibili con Direct3D</a></li>
<li><a href="supporting-dxva-2-0-in-media-foundation.md">Supporto di DXVA 2,0 in Media Foundation</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Codec hardware</td>
<td>Vedere <a href="hardware-mfts.md">hardware MFTS</a>.</td>
</tr>
<tr class="odd">
<td>Per rendere la MFT individuabile dalle applicazioni...</td>
<td>Vedere <a href="registering-and-enumerating-mfts.md">registrazione ed enumerazione di MFTS</a>.</td>
</tr>
<tr class="even">
<td>Elaborazione asincrona dei dati</td>
<td>Il modello MFT predefinito usa chiamate sincrone (bloccanti) per elaborare i dati. Per alcuni MFTs, l'elaborazione asincrona può essere più efficiente. Tuttavia, è anche più complesso da implementare.<br/> Per altre informazioni, vedere <a href="asynchronous-mfts.md">MFTS asincrono</a>.<br/></td>
</tr>
<tr class="odd">
<td>Controllo della frequenza, modalità di trick o riproduzione inversa</td>
<td>Vedere <a href="implementing-rate-control.md">implementazione del controllo della frequenza</a>.</td>
</tr>
<tr class="even">
<td>Se il MFT crea dei thread...</td>
<td>Implementare l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</td>
</tr>
<tr class="odd">
<td>Se il MFT presenta restrizioni di licenza...</td>
<td>Prendere in considerazione l'uso del meccanismo Field-of-use. Vedere il <a href="field-of-use-restrictions.md">campo relativo alle restrizioni di utilizzo</a>.</td>
</tr>
<tr class="even">
<td>Se si sta trasportando un oggetto DMO (DirectX Media Object) esistente...</td>
<td>Vedere <a href="comparison-of-mfts-and-dmos.md">confronto tra MFTS e DMOS</a>.</td>
</tr>
</tbody>
</table>



 

Questa sezione contiene i seguenti argomenti:

-   [Timestamp e durate](time-stamps-and-durations.md)
-   [Gestione delle modifiche dei flussi](handling-stream-changes.md)
-   [Implementazione di un codec MFT](implementing-a-codec-mft.md)
-   [MFTs compatibili con Direct3D](direct3d-aware-mfts.md)
-   [MFTs hardware](hardware-mfts.md)
-   [Meriti codec](codec-merit.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




