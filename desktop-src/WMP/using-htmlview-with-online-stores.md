---
title: Uso di HTMLView con i negozi online
description: Uso di HTMLView con i negozi online
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player online, HTMLView
- negozi online,HTMLView
- tipo 1 negozi online,HTMLView
- tipo 2 negozi online, HTMLView
- HTMLView, negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d5e89e2d0eaff2d51f8fa03281bf1ce85878b1863df619c28cdd228beb1eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465891"
---
# <a name="using-htmlview-with-online-stores"></a>Uso di HTMLView con i negozi online

Windows Media Player richiede agli utenti l'autorizzazione per visualizzare il contenuto HTMLView in **Now Playing**. I negozi online possono disabilitare questa richiesta specificando un valore di URL di base **nell'elemento HTMLView** del documento ServiceInfo. Quando Windows Media Player apre una playlist che specifica il contenuto HTMLView da visualizzare, player confronta l'URL di base dal documento ServiceInfo del negozio online attivo corrente all'URL di base del contenuto HTMLView. Se corrispondono, Windows Media Player il contenuto HTMLView senza chiedere conferma all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Visualizzazione di pagine Web in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento HTMLView**](htmlview-element.md)
</dt> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




