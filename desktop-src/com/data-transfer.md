---
title: Trasferimento dati
description: Trasferimento dati
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98e7f546cab245e1f2d2d06036379ea5b28526edcf42aa8a364ea04688db034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993490"
---
# <a name="data-transfer"></a>Trasferimento dati

Il Component Object Model (COM) fornisce un meccanismo standard per il trasferimento dei dati tra le applicazioni. Questo meccanismo è *l'oggetto dati*, che è semplicemente qualsiasi oggetto COM che implementa [**l'interfaccia IDataObject.**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) Alcuni oggetti dati, ad esempio una parte di testo copiato negli Appunti, hanno **IDataObject** come unica interfaccia. Altre, ad esempio oggetti documento composto, espongono diverse interfacce, di cui **IDataObject** è semplicemente una. Gli oggetti dati sono fondamentali per il funzionamento dei documenti composti, anche se hanno anche un'applicazione diffusa al di fuori di tale tecnologia OLE.

Scambiando puntatori a un oggetto dati, provider e consumer di dati possono gestire i trasferimenti di dati in modo uniforme, indipendentemente dal formato dei dati, dal tipo di supporto usato per trasferire i dati o dal dispositivo di destinazione in cui deve essere eseguito il rendering. È possibile includere il supporto nell'applicazione per i trasferimenti di base degli Appunti, i trasferimenti di trascinamento della selezione e i trasferimenti di documenti composti OLE con una singola implementazione [**di IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject). A questo punto, la quantità di codice necessaria per supportare la semantica speciale di ogni protocollo è minima.

Per altre informazioni, vedere i seguenti argomenti:

-   [Interfacce di trasferimento dati](data-transfer-interfaces.md)
-   [Formati di dati e supporti di trasferimento](data-formats-and-transfer-media.md)
-   [Trascinamento della selezione](drag-and-drop.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




