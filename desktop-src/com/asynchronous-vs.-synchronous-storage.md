---
title: Archiviazione asincrona e sincrona
description: Archiviazione asincrona e sincrona
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5662f5d9291de19fb39f044731ed72fd1db2cb04fe29d76eb785981ddeb8a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071091"
---
# <a name="asynchronous-and-synchronous-storage"></a>Archiviazione asincrona e sincrona

I moniker asincroni possono anche restituire un oggetto [Di archiviazione](/windows/desktop/Stg/asynchronous-storage) asincrona nella [**notifica IBindStatusCallback::OnDataAvailable.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) Questo oggetto di archiviazione può consentire l'accesso ad alcuni dati persistenti dell'oggetto mentre l'associazione è ancora in corso. Un client può scegliere tra due modalità per l'archiviazione: blocco e non blocco.

In modalità di blocco, compatibile con le implementazioni correnti degli oggetti di archiviazione, se i dati non sono disponibili, la chiamata si blocca fino all'arrivo dei dati. In modalità non di blocco, anziché bloccare la chiamata, l'oggetto di archiviazione restituisce un nuovo errore E PENDING quando i dati \_ non sono disponibili. Un client in grado di riconoscere l'associazione asincrona e l'archiviazione rileva questo errore e attende ulteriori notifiche ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) per ripetere l'operazione. Un client può scegliere tra un'archiviazione sincrona (bloccante) e asincrona (non di blocco) scegliendo se impostare il flag BINDF ASYNCSTORAGE nel valore \_ *grfBINDF* restituito a [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 