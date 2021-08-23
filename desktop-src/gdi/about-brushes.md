---
description: 'Esistono due tipi di pennelli: logici e fisici.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Informazioni sui pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c94ea9dac021a013ccc4ef624f9b00a3234102ac905999cb7c085148be91b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602791"
---
# <a name="about-brushes"></a>Informazioni sui pennelli

Esistono due tipi di pennelli: logici e fisici. Un *pennello logico* è una descrizione della bitmap ideale che un'applicazione usa per disegnare forme. Un *pennello fisico* è la bitmap effettiva creata da un driver di dispositivo in base alla definizione del pennello logico di un'applicazione. Per altre informazioni sulle bitmap, vedere [Bitmap.](bitmaps.md)

Quando un'applicazione chiama una delle funzioni che crea un pennello, recupera un handle che identifica un pennello logico. Quando l'applicazione passa questo handle alla [**funzione SelectObject,**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) il driver di dispositivo per lo schermo o la stampante corrispondente crea il pennello fisico.

Gli argomenti seguenti descrivono i pennelli:

-   [Origine pennello](brush-origin.md)
-   [Tipi di pennello logici](logical-brush-types.md)
-   [Trasferimento di blocchi di modelli](pattern-block-transfer.md)
-   [ICM di pennello abilitate per l'utilizzo](icm-enabled-brush-functions.md)

 

 



