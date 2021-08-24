---
description: L'attributo stretchmode specifica come estendere un'immagine che non corrisponde alle dimensioni di output.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Attributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed398fbe193ef262bdfc9a28cf66bef3a5b11f759d90c460cc99342ec7cd66b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903871"
---
# <a name="stretchmode-attribute"></a>Attributo stretchmode

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`stretchmode`L'attributo specifica come estendere un'immagine che non corrisponde alle dimensioni di output.

## <a name="possible-values"></a>Valori possibili

Deve avere uno dei valori seguenti.

-   "stretch": l'immagine viene estesa per adattarla alle dimensioni del frame di output senza mantenere le proporzioni. Valore predefinito.
-   "crop": l'immagine viene ritagliata in base alle dimensioni del frame di output.
-   "preserveaspectratio": le proporzioni originali vengono mantenute, con una casella di lettere nera lungo la dimensione più breve.
-   "preserveaspectrationoletterbox": l'immagine viene ridimensionata per riempire l'intero frame di destinazione mantenendo le proporzioni.

## <a name="applies-to"></a>Si applica a

[**clip**](clip-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



