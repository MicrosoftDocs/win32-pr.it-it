---
title: Proprietà del controllo
description: Proprietà del controllo
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856901"
---
# <a name="control-properties"></a>Proprietà del controllo

Oltre alle proprietà definite e implementate dal controllo stesso, la tecnologia dei controlli ActiveX comporta anche le operazioni seguenti:

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Proprietà di ambiente
</dt> <dd>

Queste sono esposte dal contenitore tramite un sito client di controllo per fornire valori ambientali che si applicano a tutti i controlli incorporati nel contenitore. Un contenitore, ad esempio, può fornire un colore di sfondo predefinito o un tipo di carattere predefinito che può essere utilizzato dal controllo. Le proprietà di ambiente sono esposte tramite **IDispatch** implementate sull'oggetto sito di un contenitore. Il contenitore chiama il metodo [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) del controllo quando una delle proprietà di ambiente cambia valore. In risposta, potrebbe essere necessario che un controllo aggiorni lo stato interno o di visualizzazione in risposta. Il contenitore indica quale proprietà di ambiente è stata modificata con il parametro DISPID oppure può passare il DISPID \_ Unknown per indicare che più proprietà di ambiente sono state modificate.

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Proprietà estese
</dt> <dd>

Questi vengono effettivamente implementati da un contenitore per eseguire il wrapping dei controlli in esso contenuti per fornire proprietà gestite dal contenitore visualizzate come se fossero proprietà del controllo nativo. Il contenitore può aggregare il controllo, aggiungendo le proprietà estese per completare o eseguire l'override delle proprietà del controllo. L'oggetto aggregato è denominato controllo esteso. Al contenitore, il controllo esteso viene visualizzato come il controllo stesso e le proprietà estese sembrano esposte dal controllo. Il contenitore supporta un controllo esteso tramite il metodo del sito client [**IOleControlSite:: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol). Il metodo **GetExtendedControl** consente ai controlli di spostarsi tra il sito e l'oggetto controllo esteso fornito dal contenitore, se il contenitore supporta questa funzionalità. Un contenitore può anche scegliere di visualizzare le pagine delle proprietà per i controlli estesi, oltre alle pagine che un controllo normalmente specifica tramite [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Per questo motivo, un controllo deve richiedere a un contenitore di visualizzare un frame di proprietà prima che il controllo tenti di eseguire questa operazione. Per eseguire questa operazione, il controllo chiama [**IOleControlSite:: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) . Se il contenitore implementa questa funzione, viene visualizzato il frame della proprietà. Se il metodo restituisce un errore, il controllo può visualizzare il frame della proprietà.

</dd> </dl>

Per altre informazioni, vedere i seguenti argomenti:

-   [Proprietà standard](standard-properties.md)
-   [Oggetto tipo di carattere standard](standard-font-object.md)
-   [Oggetto immagine standard](standard-picture-object.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metodi di controllo](control-methods.md)
</dt> </dl>

 

 




