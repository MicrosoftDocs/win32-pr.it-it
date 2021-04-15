---
title: Archiviazione asincrona e sincrona
description: Archiviazione asincrona e sincrona
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517158"
---
# <a name="asynchronous-and-synchronous-storage"></a>Archiviazione asincrona e sincrona

I moniker asincroni possono anche restituire un oggetto di [archiviazione asincrono](/windows/desktop/Stg/asynchronous-storage) nella notifica [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Questo oggetto di archiviazione può consentire l'accesso ad alcuni dati persistenti dell'oggetto mentre l'associazione è ancora in corso. Un client può scegliere tra due modalità per l'archiviazione: blocco e non blocco.

In modalità di blocco, che è compatibile con le implementazioni correnti degli oggetti di archiviazione, se i dati non sono disponibili, la chiamata viene bloccata fino a quando non arrivano i dati. In modalità non di blocco, anziché bloccare la chiamata, l'oggetto di archiviazione restituisce un nuovo errore E \_ in sospeso quando i dati non sono disponibili. Un client a conoscenza dell'archiviazione e dell'associazione asincrona rileva questo errore e attende altre notifiche ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) per ripetere l'operazione. Un client può scegliere tra un archivio sincrono (bloccante) e asincrono (non bloccante) scegliendo se impostare il \_ flag BINDF ASYNCSTORAGE nel valore *grfBINDF* restituito a [**IBindStatusCallback:: GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 