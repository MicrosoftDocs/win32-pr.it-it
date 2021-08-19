---
description: Perché un decodificatore non accetta il formato di input impostato?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Perché un decodificatore non accetta il formato di input impostato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7299045e41c7ec6e4c4796ed77e22c4b59af1f2c63dfc8817de8a551021f29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887041"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a>Perché un decodificatore non accetta il formato di input impostato?

Esistono diversi motivi per cui un decodificatore potrebbe rifiutare un formato. I dati in formato esteso più comuni sono mancanti o non corretti. I dati in formato esteso sono informazioni specifiche del codec che vengono aggiunte alla struttura che descrive il tipo di supporto.

Quando si enumera un tipo di output usando un oggetto codificatore, il membro **pbFormat** della [**struttura DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) farà riferimento a una **struttura WAVEFORMATEX.** A questa struttura sono stati aggiunti dati in formato esteso e le dimensioni dei dati vengono archiviate nel membro **WAVEFORMATEX.cbSize.** Indipendentemente dal contenitore usato per archiviare i dati compressi, è necessario rendere persistente la struttura **WAVEFORMATEX** e usarla nel tipo di input per il decodificatore. Senza i dati in formato esteso, il decodificatore non può decomprimere il contenuto.

Per i formati video, è necessario recuperare manualmente i dati in formato esteso e accodarlo alla **struttura VIDEOINFOHEADER.** Per altre informazioni, vedere [Uso dei dati privati del codec video.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 
