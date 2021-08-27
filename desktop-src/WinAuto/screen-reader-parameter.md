---
title: Parametro dell'utilità per la lettura dello schermo
description: Il parametro dell'utilità per la lettura dello schermo indica se un'applicazione deve fornire informazioni testuali in situazioni in cui altrimenti presenterebbe le informazioni graficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818ad36cfe833c1c9a3f39047cd88e6b4e8be55972d521ce524bb1e0618a48ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098421"
---
# <a name="screen-reader-parameter"></a>Parametro dell'utilità per la lettura dello schermo

Il parametro dell'utilità per la lettura dello schermo indica se un'applicazione deve fornire informazioni testuali in situazioni in cui altrimenti presenterebbe le informazioni graficamente.

Questo parametro viene in genere impostato dagli strumenti di accessibilità, ad esempio le utilità per la lettura dello schermo. Le applicazioni usano **i flag SPI \_ GETSCREENREADER** e **SPI \_ SETSCREENREADER** con la [**funzione SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro dell'utilità per la lettura dello schermo.

> [!Note]  
> L'Assistente vocale, l'utilità per la lettura dello schermo inclusa Windows, non imposta i flag **SPI \_ SETSCREENREADER** o **SPI \_ GETSCREENREADER.**

 

 

 