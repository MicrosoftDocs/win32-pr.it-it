---
description: DMO Requisiti minimi
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: DMO Requisiti minimi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc4f664d32112512120f2f20687051a0bff193e00adb7ad595e6975c522fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749141"
---
# <a name="dmo-minimum-requirements"></a>DMO Requisiti minimi

Ogni DMO deve soddisfare i requisiti minimi seguenti:

-   Deve supportare l'aggregazione.
-   Deve esporre [**l'interfaccia IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)
-   Il modello di threading deve essere 'both'. Gli oggetti DMO devono funzionare correttamente in un ambiente a thread libero.

Gli oggetti DMO con effetto audio devono supportare [**l'interfaccia IMediaObjectInPlace,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) per l'uso in DirectMusic e DirectSound.

Le interfacce seguenti sono documentate altrove, ma sono utili per molte dmo. Non sono tuttavia obbligatori.

-   **ISpecifyPropertyPages**, **IPropertyPage:** queste interfacce consentono a un DMO di fornire una pagina delle proprietà per consentire all'utente di impostare le proprietà.
-   **IPersistStream:** questa interfaccia consente al DMO di salvare il proprio stato in un archivio permanente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression:**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)queste interfacce consentono a un client di configurare il formato di output e le impostazioni di compressione di un codificatore. Queste due interfacce fanno parte dell'API DirectShow, ma sono consigliate anche per gli oggetti DMO.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



