---
description: Set di proprietà di avanzamento frame
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Set di proprietà di avanzamento frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746639"
---
# <a name="frame-stepping-property-set"></a>Set di proprietà di avanzamento frame

I decodificatori che implementano la ricerca con precisione dei frame in Microsoft DirectShow devono implementare il \_ \_ set di proprietà KSPROPSETID FrameStep, che viene usato insieme all'interfaccia [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .



|                   |                            |
|-------------------|----------------------------|
| GUID set di proprietà | \_FrameStep KSPROPSETID \_ |



 



| ID proprietà                              | Descrizione                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ passaggio FRAMESTEP della proprietà am \_            | Indica al decodificatore di iniziare un'operazione di passaggio e passa una struttura di [**\_ proprietà \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) che specifica il numero di passaggi.            |
| \_Proprietà am \_ FRAMESTEP \_ Cancel          | Indica al decodificatore di annullare l'operazione del passaggio corrente. Nessun dato dell'istanza è associato a questa proprietà.                                                                  |
| \_Proprietà am \_ FRAMESTEP \_ CANSTEP         | Il decodificatore restituisce \_ OK su questa istruzione per indicare che è in grado di eseguire il frame stepping, S \_ false in caso contrario. Quando questa proprietà è impostata, non vengono passati dati dell'istanza.         |
| \_Proprietà am \_ FRAMESTEP \_ CANSTEPMULTIPLE | Il decodificatore restituisce \_ OK in questa istruzione per indicare che è possibile eseguire più frame alla volta, in \_ caso contrario, s false. Quando questa proprietà è impostata, non vengono passati dati dell'istanza. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 



