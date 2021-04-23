---
description: Set di proprietà Frame Stepping
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Set di proprietà Frame Stepping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908449"
---
# <a name="frame-stepping-property-set"></a>Set di proprietà Frame Stepping

I decodificatori che implementano la ricerca accurata dei frame in Microsoft DirectShow devono implementare il set di proprietà \_ AM KSPROPSETID FrameStep, che viene usato insieme \_ all'interfaccia [**IVideoFrameStep.**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)



| Label | Valore |
|-------------------|----------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ FrameStep |



 



| ID proprietà                              | Descrizione                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ FRAMESTEP \_ STEP            | Indica al decodificatore di iniziare un'operazione di passaggio e passa una struttura [**\_ AM PROPERTY \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) che specifica il numero di passaggi.            |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL          | Indica al decodificatore di annullare l'operazione del passaggio corrente. Nessun dato dell'istanza è associato a questa proprietà.                                                                  |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP         | Il decodificatore restituisce S OK in questa istruzione per indicare che è possibile eseguire l'esecuzione delle istruzioni dei \_ frame, S \_ FALSE in caso contrario. Quando questa proprietà è impostata, non viene passato alcun dato dell'istanza.         |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE | Il decodificatore restituisce S OK in questa istruzione per indicare che può eseguire più fotogrammi \_ alla volta, S \_ FALSE in caso contrario. Quando questa proprietà è impostata, non viene passato alcun dato dell'istanza. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 



