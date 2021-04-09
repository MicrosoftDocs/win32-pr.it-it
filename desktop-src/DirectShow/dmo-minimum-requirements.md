---
description: Requisiti minimi DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Requisiti minimi DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965747"
---
# <a name="dmo-minimum-requirements"></a>Requisiti minimi DMO

Ogni DMO deve soddisfare i requisiti minimi seguenti:

-   Deve supportare l'aggregazione.
-   Deve esporre l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .
-   Il modello di threading deve essere ' both '. DMOs deve funzionare correttamente in un ambiente a thread libero.

L'effetto audio DMOs deve supportare l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , da usare in DirectMusic e DirectSound.

Le interfacce seguenti sono documentate altrove, ma sono utili per molti DMOs. Tuttavia, non sono necessarie.

-   **ISpecifyPropertyPages**, **IPropertyPage**: queste interfacce consentono a DMO di fornire una pagina delle proprietà per consentire all'utente di impostare le proprietà.
-   **IPersistStream**: questa interfaccia consente a DMO di salvare lo stato nell'archivio permanente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): queste interfacce consentono a un client di configurare il formato di output del codificatore e le impostazioni di compressione. Queste due interfacce fanno parte dell'API DirectShow, ma sono consigliate anche per DMOs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



