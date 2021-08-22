---
description: Set di proprietà Frame Stepping
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Set di proprietà Frame Stepping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ccddab4cd7f302dc850a4581ce8e70dcffc9cb6a4943c8f768a74c890edfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565001"
---
# <a name="frame-stepping-property-set"></a>Set di proprietà Frame Stepping

I decodificatori che implementano la ricerca accurata dei frame in Microsoft DirectShow devono implementare il set di proprietà AM \_ KSPROPSETID \_ FrameStep, usato insieme all'interfaccia [**IVideoFrameStep.**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)



| Etichetta | Valore |
|-------------------|----------------------------|
| GUID set di proprietà | FrameStep \_ di AM KSPROPSETID \_ |



 



| ID proprietà                              | Descrizione                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PASSAGGIO \_ DEL PASSAGGIO DEL PASSAGGIO DEL FRAME DI PROPRIETÀ \_ \_ AM            | Indica al decodificatore di iniziare un'operazione di passaggio e passa una struttura [**AM \_ PROPERTY \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) che specifica il numero di passaggi.            |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL          | Indica al decodificatore di annullare l'operazione del passaggio corrente. Nessun dato dell'istanza è associato a questa proprietà.                                                                  |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP         | Il decodificatore restituisce S OK su questa istruzione per indicare che può eseguire l'esecuzione di \_ istruzioni dei fotogrammi, S \_ FALSE in caso contrario. Quando questa proprietà è impostata, non viene passato alcun dato di istanza.         |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE | Il decodificatore restituisce S OK in questa istruzione per indicare che può eseguire più \_ fotogrammi contemporaneamente, S \_ FALSE in caso contrario. Quando questa proprietà è impostata, non viene passato alcun dato di istanza. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 



