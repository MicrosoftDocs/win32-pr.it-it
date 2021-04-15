---
title: Trasferimento dati
description: Trasferimento dati
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516066"
---
# <a name="data-transfer"></a>Trasferimento dati

Il Component Object Model (COM) fornisce un meccanismo standard per il trasferimento dei dati tra le applicazioni. Questo meccanismo è l' *oggetto dati*, che è semplicemente un oggetto com che implementa l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Alcuni oggetti dati, ad esempio una porzione di testo copiata negli Appunti, hanno **IDataObject** come unica interfaccia. Altri, ad esempio oggetti documento composito, espongono diverse interfacce, di cui **IDataObject** è semplicemente uno. Gli oggetti dati sono fondamentali per l'utilizzo di documenti composti, sebbene abbiano anche un'applicazione diffusa al di fuori della tecnologia OLE.

Scambiando i puntatori a un oggetto dati, i provider e i consumer di dati possono gestire i trasferimenti di dati in modo uniforme, indipendentemente dal formato dei dati, dal tipo di supporto usato per trasferire i dati o dal dispositivo di destinazione in cui deve essere eseguito il rendering. È possibile includere il supporto nell'applicazione per i trasferimenti di base degli Appunti, i trasferimenti con trascinamento della selezione e i trasferimenti di documenti compositi OLE con una singola implementazione di [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). Una volta eseguita questa operazione, la quantità di codice necessaria per gestire la semantica speciale di ogni protocollo è minima.

Per altre informazioni, vedere i seguenti argomenti:

-   [Interfacce di Trasferimento dati](data-transfer-interfaces.md)
-   [Formati di dati e supporti di trasferimento](data-formats-and-transfer-media.md)
-   [Trascinamento della selezione](drag-and-drop.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




