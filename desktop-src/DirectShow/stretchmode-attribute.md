---
description: L'attributo stretchmode specifica come estendere un'immagine che non corrisponde alle dimensioni di output.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Attributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883729"
---
# <a name="stretchmode-attribute"></a>Attributo stretchmode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `stretchmode` attributo specifica come estendere un'immagine che non corrisponde alle dimensioni di output.

## <a name="possible-values"></a>Valori possibili

Deve avere uno dei valori seguenti.

-   "Stretch": l'immagine viene adattata alle dimensioni del frame di output senza mantenere le proporzioni. Valore predefinito.
-   "Crop": l'immagine viene ritagliata per adattarsi alle dimensioni del frame di output.
-   "PreserveAspectRatio": le proporzioni originali vengono mantenute, con una letterbox nera lungo la dimensione più breve.
-   "preserveaspectrationoletterbox": l'immagine viene ridimensionata per riempire l'intero frame di destinazione mantenendo le proporzioni.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



