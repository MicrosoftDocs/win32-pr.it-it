---
title: Parametro Visualizzatore schermo
description: Il parametro screen reader indica se un'applicazione deve fornire informazioni testuali in situazioni in cui in caso contrario le informazioni verranno presentate graficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047016"
---
# <a name="screen-reader-parameter"></a>Parametro Visualizzatore schermo

Il parametro screen reader indica se un'applicazione deve fornire informazioni testuali in situazioni in cui in caso contrario le informazioni verranno presentate graficamente.

Questo parametro viene in genere impostato da strumenti di accessibilità, ad esempio utilità per la lettura dello schermo. Le applicazioni usano i flag **SPI \_ GETSCREENREADER** e **SPI \_ SETSCREENREADER** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di lettura dello schermo.

> [!Note]  
> Assistente vocale, lo screen reader incluso in Windows, non imposta i flag **SPI \_ SETSCREENREADER** o **SPI \_ GETSCREENREADER**

 

 

 